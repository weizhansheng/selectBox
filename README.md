# selectBox

依赖jQuery，兼容IE8+ & 其他浏览器

## 结构

1.  纯原生Select
```html
<select id="select_id" style="display: none;">
    <option value="1">测试1</option>
    <option value="2">测试2</option>
    <option value="3">测试3</option>
 </select>
 ```
 2.  div+dl>dd
 ```html
 <div id="div_id">
     <div class="select-box-inner">
         <input type="text" class="select-text">
     </div>
     <dl>
         <dd data-id="1">测试1</dd>
         <dd data-id="2">测试2</dd>
         <dd data-id="3">测试3</dd>
     </dl>
 </div>
 ```
 3.  纯div，jsAPI初始化数据
 ```html
 <div id="div_id"></div>
 ```
 实例化后DOM结构如下
 ```html
 <div class="select-box" id="div_id">
     <div class="select-box-inner">
         <input type="text" class="select-text">
     </div>
     <dl>
         <dd data-id="1">测试1</dd>
         <dd data-id="2">测试2</dd>
         <dd data-id="3">测试3</dd>
     </dl>
 </div>
 <select id="select_id" style="display: none;">
    <option value="1">测试1</option>
    <option value="2">测试2</option>
    <option value="3">测试3</option>
 </select>
```
## 方法

* var instance = $('#select_id').selectBox()<br>  原生select实例化
* var instance = $('#div_id').selectBox()<br>  div.select-box实例化，值初始化在dl>dd
* instance.setOptions([{},{},{}])<br>  用于级联操作情况下重置数据
* instance.val()<br>  得到当前选中对象数据（JSON）
* instance.val('value')<br>  传入value，设置为当前选中值
* instance.disable()<br>  禁用select实例
* instance.enable()<br>  启用select实例
* instance.destroy()<br>  销毁实例
* instance.refresh()<br>  恢复select实例初始状态
