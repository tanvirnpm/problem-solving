let num = 4587;
const arr = []
while(num > 0){
  // console.log( num % 10);
  const mod = num % 10;
  console.log(mod);
  num = Math.floor(num / 10);
  arr.push(''+mod)
}
arr.join('')
