var matrix = function(x){ 
	this.x = x;
	
	this.tran=function(){
	var tmp = [];
	var x=this.x;
	for(var j = 0; j < x[0].length; j++){
		tmp[j] = [];
		for(var i = 0; i < x.length; i++){
			tmp[j][i] = x[i][j];
		}
	}
	return new matrix(tmp);
}

        this.add=function(x){
	var tmp = [];
	var x= this.x;
	for(var i = 0; i < x.length; i++){
		tmp[i] = [];
		for(var j = 0; j < x[i].length; j++){
			tmp[i][j] = x[i][j] + x[i][j];
		}
	}
	return new matrix(tmp);
}
        this.time=function(y){
	var tmp = [];
	var sum = 0;
	var x = this.x;
	for(var i = 0; i < x.length; i++){
		tmp[i] = [];
		for(var j = 0; j < y.x[i].length; j++){
			tmp[i][j] = 0;
			for(var k = 0; k < x[i].length; k++){
				tmp[i][j] = tmp[i][j] + x[i][k] * y.x[k][j];
			}
		}
	}
	return new matrix(tmp);
}
}

var a = new matrix([[3,2,1],[1,2,3]]);
var b = a.tran();
var c = a.add(a);
var d = a.time(b);

console.log("a = %j", a);
console.log("b = %j", b);
console.log("c = %j", c);
console.log("d = %j", d);
