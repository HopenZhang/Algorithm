# Algorithm
The foundation of computer programs.<br>
![](http://bpic.588ku.com/element_origin_min_pic/16/09/22/1957e3c3e2a4280.jpg)
<h2>Array的添加和删除</h2>
<ul>
  <li>
    <h4>shift：删除原数组第一项，并返回删除元素的值；如果数组为空则返回undefined</h4>
    var a = [1,2,3,4,5];<br/>
    var b = a.shift(); &nbsp;&nbsp; //a：[2,3,4,5]  &nbsp;&nbsp;   b：1 
  </li>
  <li>
    <h4>unshift：将参数添加到原数组开头，并返回数组的长度</h4>
    var a = [1,2,3,4,5]; <br/>
    var b = a.unshift(-2,-1); &nbsp;&nbsp; //a：[-2,-1,1,2,3,4,5]  &nbsp;&nbsp;  b：7 <br/>
    注：在IE6.0下测试返回值总为undefined，FF2.0下测试返回值为7，所以这个方法的返回值不可靠，需要用返回值时可用splice代替本方法来使用。 
  </li>
  <li>
    <h4>pop：删除原数组最后一项，并返回删除元素的值；如果数组为空则返回undefined </h4>
    var a = [1,2,3,4,5];<br/>
    var b = a.pop();&nbsp;&nbsp; //a：[1,2,3,4] &nbsp;&nbsp;  b：5 &nbsp;&nbsp; //不用返回的话直接调用就可以了
  </li>
  <li>
    <h4>push：将参数添加到原数组末尾，并返回数组的长度 </h4>
    var a = [1,2,3,4,5]; <br/>
    var b = a.push(6,7); &nbsp;&nbsp; //a：[1,2,3,4,5,6,7] &nbsp;&nbsp;  b：7 
  </li>
  <li>
    <h4>concat：返回一个新数组，是将参数添加到原数组中构成的 </h4>
    var a = [1,2,3,4,5]; <br/>
    var b = a.concat(6,7); &nbsp;&nbsp; //a：[1,2,3,4,5] &nbsp;&nbsp;  b：[1,2,3,4,5,6,7]  
  </li>
  <li>
    <h4>splice(start,deleteCount,val1,val2,...)：从start位置开始删除deleteCount项，并从该位置起插入val1,val2,... </h4>
    var a = [1,2,3,4,5]; <br/>
    var b = a.splice(2,2,7,8,9); &nbsp;&nbsp; //a：[1,2,7,8,9,5]  &nbsp;&nbsp; b：[3,4] <br/>
    var b = a.splice(0,1); &nbsp;&nbsp; //同shift <br/>
    a.splice(0,0,-2,-1); &nbsp;&nbsp; var b = a.length; &nbsp;&nbsp; //同unshift <br/>
    var b = a.splice(a.length-1,1); &nbsp;&nbsp; //同pop <br/>
    a.splice(a.length,0,6,7); &nbsp;&nbsp; var b = a.length; &nbsp;&nbsp; //同push 
  </li>
  <li>
    <h4>reverse：将数组反序 </h4>
    var a = [1,2,3,4,5]; <br/>
    var b = a.reverse();&nbsp;&nbsp; //a：[5,4,3,2,1] &nbsp;&nbsp;  b：[5,4,3,2,1]  
  </li>
  <li>
    <h4>sort(orderfunction)：按指定的参数对数组进行排序 </h4>
    var a = [1,2,3,4,5]; <br/>
    var b = a.sort();&nbsp;&nbsp; //a：[1,2,3,4,5] &nbsp;&nbsp;  b：[1,2,3,4,5] 
  </li>
  <li>
    <h4>slice(start,end)：返回从原数组中指定开始下标到结束下标之间的项组成的新数组 </h4>
    var a = [1,2,3,4,5]; <br/>
    var b = a.slice(2,5);&nbsp;&nbsp; //a：[1,2,3,4,5] &nbsp;&nbsp;  b：[3,4,5] 
  </li>
  <li>
    <h4>join(separator)：将数组的元素组起一个字符串，以separator为分隔符，省略的话则用默认用逗号为分隔符 </h4>
    var a = [1,2,3,4,5]; <br/>
    var b = a.join("|");&nbsp;&nbsp; //a：[1,2,3,4,5] &nbsp;&nbsp;  b："1|2|3|4|5"
  </li>
</ul>
&nbsp;&nbsp;&nbsp;&nbsp;[引用原文](http://www.cnblogs.com/gxlinhai/p/5233734.html)<br /> 
