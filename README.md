# call-apply
本文将详细描述call和apply的用途，相同点和不同点

Function.prototype.call和Function.prototype.apply都是非常常用的方法。他们的作用一模一样，区别仅仅在于传递参数的形式不同。

apply接受两个参数，第一个参数指定函数体内this对象的指向，第二个参数为一个带下标的集合，这个集合可以为数组，也可以为类数组。

call传入的参数数量不固定,第一个参数指定函数体内this对象的指向,从第二个参数开始往后，每一个参数被依次传入函数。

当使用call或者apply的时候，如果我们传入的第一个参数为null，函数体内的this会指向默认的宿主对象，在浏览器中则是window;但是在严格模式下，函数体内的this还是为null;

call和apply在实际开发中的用途
1.改变this的指向

var obj1={
    name:'seven'    
};

var obj2={
    name:'anne'
};

window.name='window';

var getName=function(){
  console.debug(this.name);
}
getName();输出window
getName.call(obj1); 输出seven
getName.call(obj2); 输出anne
