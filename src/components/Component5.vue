<!-- 父子组件通信，点击父控件输出子组件中的方法 -->
<template>
<div class='bbb'>
    <div>child内容</div>
</div>
</template>

<script>

export default {
name:'say-hello',
components: {},
data() {
//这里存放数据
return {
    name:"我是child",
};
},
//监听属性 类似于data概念
computed: {},
//监控data中的数据变化
watch: {},
//方法集合
methods: {
    sayHello()
    {
        console.log("hello");
        alert("hello");
    }
},
//生命周期 - 创建完成（可以访问当前this实例）
created() {

},
//生命周期 - 挂载完成（可以访问DOM元素）
mounted() {

},
beforeCreate() {}, //生命周期 - 创建之前
beforeMount() {}, //生命周期 - 挂载之前
beforeUpdate() {}, //生命周期 - 更新之前
updated() {}, //生命周期 - 更新之后
beforeDestroy() {}, //生命周期 - 销毁之前
destroyed() {}, //生命周期 - 销毁完成
activated() {}, //如果页面有keep-alive缓存功能，这个函数会触发
}
</script> 