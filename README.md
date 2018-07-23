# lecture9--task-js
// map task


var myarry = [10, 15, 18, 20, 45, 34, 42, 56];
function myMapfun(value, cb) {
	var Arry = [];

	for (var i = 0; i < value.length; i++) {
		Arry.push(cb(value[i]));
	}
	return Arry;
}

var arr1 = myMapfun(myarry, function(value) {
	return value + 10;
});

var arr2 = myMapfun(myarry, function(value) {
	return value - 10;
});
var arr3 = myMapfun(myarry, function(value) {
	return value * 2;
});
var arr4 = myMapfun(myarry, function(value) {
	return value / 2;
});
console.log('my map sum function value:', arr1);
console.log('my map sub function value', arr2);
console.log('my map mul function value', arr3);
console.log('my map division function value', arr4);


// object task....

var obj={
    name: 'sujoy',
    lastName:'saha',
    age:23,
    gender:'meal',
   skill:['js','html','css']

}

function Dowhateveryouwant(person, cb){  
    return cb(person);
}
var information = Dowhateveryouwant(obj, function(data){    
    return data.skill;    
})
console.log('My information is ' + information);
