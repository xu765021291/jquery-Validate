# jquery-validation
  > 专门用于表单验证的jquery插件  
  > [github](https://github.com/naver/billboard.js)
  > [官方](https://jqueryvalidation.org/)

## 如何使用?
  1. 下载jquery-validation
  > 可以通过npm 下载: `npm install jquery-validation`
  2. 新建一个html文件,如: `index.html`，添加如下代码:  
  ```html
  <!--1.在form中加入一个input, 【注意】input中添加了一个required属性，表示该input中的内容不能为空-->
  <form>
    <input type="text" required>
  </form>
  <!-- 2.引入jquery 来 jquery-validation -->
  <script src="./node_modules/jquery/dist/jquery.js"></script>
  <script src="./node_modules/jquery-validation/dist/jquery.validate.js"></script>
  <script>
    // 3.初化表单验证插件
    $('form').validate()
  </script>
  ```
  > 尝试着在浏览器中打开该`index.html`查看效果  
  > 提交下表单试试(可以通过在input中按下【回车键】来触发表单提交事件)  
  > ![效果图](./images/basic.jpg)

### 各个属性说明
  1	required:true	必须输入的字段。
  2	remote:"check.php"	使用 ajax 方法调用 check.php 验证输入值。
  3	email:true	必须输入正确格式的电子邮件。
  4	url:true	必须输入正确格式的网址。
  5	date:true	必须输入正确格式的日期。日期校验 ie6 出错，慎用。
  6	dateISO:true	必须输入正确格式的日期（ISO），例如：2009-06-23，1998/01/22。只验证格式，不验证有效性。
  7	number:true	必须输入合法的数字（负数，小数）。
  8	digits:true	必须输入整数。
  9	creditcard:	必须输入合法的信用卡号。
  10	equalTo:"#field"	输入值必须和 #field 相同。
  11	accept:	输入拥有合法后缀名的字符串（上传文件的后缀）。
  12	maxlength:5	输入长度最多是 5 的字符串（汉字算一个字符）。
  13	minlength:10	输入长度最小是 10 的字符串（汉字算一个字符）。
  14	rangelength:[5,10]	输入长度必须介于 5 和 10 之间的字符串（汉字算一个字符）。
  15	range:[5,10]	输入值必须介于 5 和 10 之间。
  16	max:5	输入值不能大于 5。
  17	min:10	输入值不能小于 10。