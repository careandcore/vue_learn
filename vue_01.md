# vue
- 前端三大框架：vue，angular，react
- 渐进式javascript框架：不需要从全家桶开始使用，前后端可以不一样

##基本语法
    1、 v-bind  绑定属性
    2、 v-on    绑定事件
    3、 v-model 绑定变量，双向绑定
## vue 的生命周期
![vue生命周期](./vue生命周期.png)

    1、 vue的生命周期是什么？
        vue每一个组件都是独立的，每一个组件都有一个属于它自己的生命周期，从一个组件创建、数据初始化、挂载、更新、销毁，这就是一个组件所谓的生命周期。在组件中具体的方法有:
        beforecreate,created,beforemount,mounted,beforeupdate,updated,beforedestory,destoryed
    2、 执行流程：
        1、做初始化工作
        2、执行beforecreate钩子函数（如果有）
        3、初始化data数据
        4、执行created钩子函数（如有）
        5、判断是否传了el选项
        6、如果没有传，则等到实例vm主动调用$mount()再继续执行
        7、如果传了el，再判断是否有传template模板选项
        8、如果没有传template，则将el对应的所有内容当成template
        9、将template通过render函数编译成vdom虚拟DOM树
        10、执行beforeMount钩子函数（如果有）
        11、将虚拟DOM替换掉el容器中的旧内容（把真正的HTML覆盖掉模板）
        12、执行mounted钩子函数（如有）
        13、当data数据发生改变时，先走beforeupdate，VDOM更新完后，走update
        14、当组件切换或者跳转路由时，或手动销毁vue实例的时候调用beforedestory钩子函数（如有）
        15、解除事件绑定，销毁子组件
        16、执行destory钩子函数（如有）

        
# 设置class语法


# axios语法
    axios.get(url,{}).then(function(res){
        res.data
    })
## 计算属性
    computed：一个变量的值依赖于其他变量

## 监听事件
    watch：某个变量改变后触发某些动作（函数）
## 地址栏操作

## 组件
    1、components ：用来放置组件对象
    2、template ：模板对象
    3、props ：接收调用者传递的参数  
    4、refs ：组件标识
    5、常用属性
        $children   $parent $refs

# webpack
    1、npm init -y
    2、npm install webpack webpack-cli --save-dev
    3、cnpm install --save-dev clean-webpack-plugin ：删除老的dist文件 ，再生成新的
    4、cnpm install --save-dev html-webpack-plugin  :生成html
    5、cnpm install --save-dev file-loader   ：将图片打包
    6、cnpm install --save-dev url-loader ：
    7、vue-loader


# npm 使用
    1、下载node.js
    2、参考https://zhuanlan.zhihu.com/p/92707747

# vue-cli使用
    1、安装
        npm install -g @vue/cli
    2、创建一个项目
        vue create my-project
    3、运行