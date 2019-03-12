dom event(事件)
- dom
    onclick  事件注册只有一个，后面的覆盖前面的       dom0标准
    addEventListener('click')  不限                 dom2标准
    addEventListener('keyup')  不限                 dom3标准
    addEventListener('click',function(){},true|false)       true为捕获,false为冒泡
- event
    event.stopProgration()              阻止父元素事件冒泡
    event.stopImmediatePropagation();   阻止后面注册的所有事件
- dom事件流
    捕获(capture) 点击子元素 父元素事件也会调用     (冒泡bubble  顺序相反)
    window->document.documentElement->body->父级->目标元素

    事件按照 dom流的顺序执行我们的事件回调  先捕获再冒泡
    处于目标阶段时,事件调用顺序取决于事件注册的顺序

- 事件代理(事件委托)
    event-question.html  原理:事件冒泡