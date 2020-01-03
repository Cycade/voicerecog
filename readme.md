# 简单的语音识别插件

## 使用场景
#### 在用户选中（过）某个输入框时，直接将语音转换出的文字添加到该输入框中，并向用户提供复制识别结果的选项
1. 页面加载完毕后向不存在 id 的 input/textarea 添加随机字符串作为 id，并添加 onfocus 事件
2. 如果用户 focus 了一个 input/textarea，就把该元素的 id 添加进 localStorage
3. 在语音识别完毕后，对页面中的 input/textarea 逐一比对。如 id 相等，则改变其中内容
4. 如果未改变任何内容，如 DOM 发生了变动，则鼓励用户将识别内容复制到剪贴板

#### 在用户未曾选过任何输入框时，或当前页面没有输入框时，提醒用户相关内容已复制到剪贴板
直接提示用户相关内容已复制到剪贴板

## 改进方向
1. 使用 react 重写 popup 页，更有利于管理状态，节省逻辑。
2. 为用户提供识别的可选项，从高到底排列，供用户选择。
3. 给出设置页，用户可以自行更改设置，如提供多语言选项