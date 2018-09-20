# Object.assign-
ES6 对象提供了Object.assign()这个方法来实现浅复制


Object.assign() 方法用于将所有可枚举属性的值从一个或多个源对象复制到目标对象。它将返回目标对象。

  描述:
         如果目标对象中的属性具有相同的键，则属性将被源中的属性覆盖。后来的源的属性将类似地覆盖早先的属性。

           Object.assign 方法只会拷贝源对象自身的并且可枚举的属性到目标对象。该方法使用源对象的[[Get]]和目标对象的[[Set]]，
           所以它会调用相关 getter 和 setter。
           因此，它分配属性，而不仅仅是复制或定义新的属性。如果合并源包含getter，这可能使其不适合将新属性合并到原型中。
           为了将属性定义（包括其可枚举性）复制到原型，应使用Object.getOwnPropertyDescriptor()和Object.defineProperty() 。  
           
           
  注意，Object.assign 不会跳过那些值为 null 或 undefined 的源对象。   
     
     
 例子：
        
           const object1 = {
              a: 1,
              b: 2,
              c: 3,
              k:8000
            };

            const object2 = Object.assign({c: 4, d: 5}, object1);

            console.log(object2.c, object2.d,object2.k);  //  3 5 8000
            console.log(object2.a)  //1
            
  复制一个对象

        var obj = { a: 1 };
        var copy = Object.assign({}, obj);
        console.log(copy); // { a: 1 }


         
         
          


























