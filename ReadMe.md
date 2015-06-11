#自用Array扩展
```javascript
/**
 * 在指定位置插入元素
 * @param  {Number} i    目标位置，下标从0开始
 * @param  {Object} item 插入元素
 */
Array.prototype.insert = function(i,item){
    this.splice(i,0,item);
}
//Example
var arr = ['a','b','e','f','g',1,2,3];
arr.insert(2,'d');
console.log(arr);//['a','b','d','e','f','g',1,2,3];
```


```javascript
Array.prototype.clone = function(){
    return this.slice(0);
};
//Example
var arr = ['a','b','e','f','g',1,2,3],
    b = arr.clone(2,'d');
console.log(b);//['a','b','e','f','g',1,2,3]
```


```javascript
Array.prototype.empty = function(){
    this.length = 0;
};
//Example
var arr = ['a','b','e','f','g',1,2,3];
arr.clear();
console.log(arr);//[]
```


```javascript
Array.prototype.remove = function(item){
    for(var i = this.length-1; i--;){
        if(this[i] === item ) this.splice(i, 1);
    }
};
//Example
var arr = ['a','b','e','f','g',1,2,3];
arr.remove('a');
console.log(arr);//['b','e','f','g',1,2,3];
```