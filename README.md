# Vue-learn
总结 记忆一些遗忘的知识点

* **1.v-if="sceen"    可以根据sceen的boolean值操作当前dom是否可见。**
  * v-else/v-else-if    
    v-if是动态的向DOM树内添加或者删除DOM元素； 
    v-show是通过设置DOM元素的display样式属性控制显隐； 
  
* **2. v-once 指令**
  * 执行一次性地插值，当数据改变时，插值处的内容不会更新。但请留心这会影响到该节点上所有的数据绑定：      
    ‘<span v-once>这个将不会改变 {{msg}}</span>’

* **3. v-methods/computed **
  * methods: 调用方法需要 function()   —--没有缓存
    computed: 调用方法需要 function    ——有缓存

* **4. watch **
  * 来响应数据的变化，数据变化调用。 watch中函数名必须与data中名一致。参数是变化的数据

* **5. v-methods/computed **
  * methods: 调用方法需要 function()   —--没有缓存
    computed: 调用方法需要 function    ——有缓存

* **6. beforeUpdate/updated **
  * data 值改变触发。在钩子函数中mounted修改data值可以触发。之前的钩子不能触发

* **7. props如何传值给data**
  * 在data里面设置的时候只能设置初始值，所以如果想要在值改变的时候跟着改变，可以watch一下，然后在watch里面做更新操作。
  * [‘props’]值可以应用在data中、应用在模板中、可以应用在方法中。

* **8. 全局注册组件 必须在根实例（通过new Vue）创建之前发生。 **
  *

* **9. 在一个组件的根元素上直接监听一个原生事件 **
  * 这时，你可以使用 v-on 的 .native 修饰符
  * 注意： 这个原生事件是指 template中的根元素
  * 例： ‘<base-input v-on:focus.native="onFocus"></base-input>’ 参考：https://cn.vuejs.org/v2/guide/components-custom-events.html

* **10. 组件中 data 必须是一个函数**
  * data: function () {
        return {
            count: 0
        }
    }
  
