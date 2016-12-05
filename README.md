# call-apply
本文将详细描述call和apply的用途，相同点和不同点

Function.prototype.call和Function.prototype.apply都是非常常用的方法。他们的作用一模一样，区别仅仅在于传递参数的形式不同。

apply接受两个参数，第一个参数指定函数体内this对象的指向，第二个参数为一个带下标的集合，这个集合可以为数组，也可以为类数组。

call传入的参数数量不固定,第一个参数指定函数体内this对象的指向,从第二个参数开始往后，每一个参数被依次传入函数。

当
