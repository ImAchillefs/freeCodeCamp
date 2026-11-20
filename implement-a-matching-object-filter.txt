** start of script.js **

function whatIsInAName(arr, obj) {
  return arr.filter((key, index) => {
    let keyCount=0;
    for (let i in key) {
      keyCount++
    }
    let objCount=0;
    for(let i in obj) {
      objCount++;
    }
    for (let j=0; j<keyCount; j++){
      let correctionCount=0;
      for (let k in key){
        if (key[k]===obj[k]){
          correctionCount++;
        }
      }
      console.log(correctionCount,keyCount,objCount, key)
      if (correctionCount <= keyCount && correctionCount >= objCount) {
        return true;
      }
    }
  })
}

//use the index function to check if logical operation is happening on the same object, so that you prevent double logging to the console


console.log(whatIsInAName([{ "apple": 1, "bat": 2 }, { "apple": 1 }, { "apple": 1, "bat": 2, "cookie": 2 }], { "apple": 1, "cookie": 2 }))

** end of script.js **

