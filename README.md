1.var obj1 = { name: "Person 1", age:5 };
  var obj2 = { age:5, name: "Person 1" };

  console.log(obj1===obj2)
  
  
  
  ===============================================================================================================================================================================
  ===============================================================================================================================================================================
  
  
2.var req = new XMLHttpRequest();
req.open('GET','https://restcountries.eu/rest/v2/all',true);
req.send();
req.onload=function(){
    var data = JSON.parse(this.response);
     
    for(let i in data){
        console.log(`flag: ${data[i].flag}`);
           }
   
}



===============================================================================================================================================================================
===============================================================================================================================================================================



3.const getcountries= () => {
  const xhr =new XMLHttpRequest();
  xhr.open('GET','https://restcountries.eu/rest/v2/all');
  xhr.reponseType="JSON"

xhr.onload=()=>{
  const countries=xhr.response;
  console.log(countries)
  
  const result = JSON.parse(countries)

  .map((countries) => ({name:countries.name, region:countries.region,subregion:countries.subregion,population:countries.population}))
console.log(result)
  }

xhr.send()
}
getcountries();














































