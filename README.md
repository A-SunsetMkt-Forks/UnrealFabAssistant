# UnrealFabAssistant

简体中文 | [English](/doc/README_EN.md)

把所有虚幻Fab商城免费资产一键入库（可隔一段时间跑一次，自动入库最新的免费资源）

>Note: 代码仅在chrome上测试通过，最好直接使用chrome

### 如何使用

#### 方式1
1. 打开油猴设置-实用工具
2. 在**从URL安装**中粘贴以下链接导入
3. 打开 [Fab](https://www.fab.com/)，右下角小窗点击Start，等待完成
```javascript
https://raw.githubusercontent.com/RyensX/UnrealFabAssistant/refs/heads/main/tampermonkey.js
```

如果无法访问魔法网络，可以用下方链接（更新可能有延迟）
```javascript
https://gh-proxy.com/raw.githubusercontent.com/RyensX/UnrealFabAssistant/refs/heads/main/tampermonkey.js
```

#### 方式2
1. 打开 [Fab](https://www.fab.com/) 并登录
2. 点击F12打开调试工具并切换到控制台（Console）tab
3. 复制粘贴下面代码回车等待结束
```javascript
fetch('https://raw.githubusercontent.com/RyensX/UnrealFabAssistant/refs/heads/main/run.js').then(r=>r.text()).then(t=>document.head.append(Object.assign(document.createElement('script'),{textContent:t})))
```

如果无法访问魔法网络，可以用下方链接（更新可能有延迟）

```javascript
fetch('https://gh-proxy.com/raw.githubusercontent.com/RyensX/UnrealFabAssistant/refs/heads/main/run.js').then(r=>r.text()).then(t=>document.head.append(Object.assign(document.createElement('script'),{textContent:t})))
```

#### 方式3
1. 打开[run.js](/run.js)复制全部代码到剪切板
2. 打开 [Fab](https://www.fab.com/) 并登录
4. 点击F12打开调试工具并切换到控制台（Console）tab
5. 粘贴刚才复制的代码到输入框，然后回车
6. 等待日志打印结束即完成入库

### 已知问题
- 请求过多提示 "Too many requests."
    - 如果已经完成所有入库则无需理会
    - 如果没有，则等待几分钟，然后重试

### 鸣谢
- https://gist.github.com/jamiephan/0c04986c7f2e62d5c87c4e8c8ce115fc

### 其他
1. 若有帮助到您，请点击右上角⭐支持一下，感谢使用
2. 如果进行转载，请注明原出处 https://github.com/RyensX/UnrealFabAssistant
3. 默认快速模式以时间降序查询物品，若超过3页都没有能添加的物品，则认为该分类已经没有新增的，这可能会错过一些旧的资源突然免费的情况，但是可以方便频繁快速白嫖资源。如果需要关闭快速模式，可以运行前控制台执行 **window.fastMode=false**