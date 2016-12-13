# Algorithm
&nbsp;&nbsp;&nbsp;&nbsp;The foundation of computer programs.<br><br>
![](http://bpic.588ku.com/element_origin_min_pic/16/09/22/1957e3c3e2a4280.jpg)
<h2>Array的添加与删除</h2>
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
    <h4>concat：返回一个新数组，将参数添加到原数组中构成新数组 </h4>
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
    <h4>slice(start,end)：返回从原数组中指定开始下标到结束下标之间的项组成的新数组 </h4>
    var a = [1,2,3,4,5]; <br/>
    var b = a.slice(2,5);&nbsp;&nbsp; //a：[1,2,3,4,5] &nbsp;&nbsp;  b：[3,4,5] 
  </li>
</ul>
&nbsp;&nbsp;&nbsp;&nbsp;[引用原文](http://www.cnblogs.com/gxlinhai/p/5233734.html)<br /> 
<h2>Array的其他方法</h2>
<ul>
  <li>
    <h4>join(separator)：将数组的元素组起一个字符串，以separator为分隔符，省略的话则用默认用逗号为分隔符 </h4>
    var a = [1,2,3,4,5]; <br/>
    var b = a.join("|");&nbsp;&nbsp; //a：[1,2,3,4,5] &nbsp;&nbsp;  b："1|2|3|4|5"
  </li>
  <li>
    <h4>split(separator,howmany)：将一个字符串分割成字符串数组 </h4>
    var b = "1|2|3|4|5"; <br/>
    var a = b.split("|");&nbsp;&nbsp; //a：[1,2,3,4,5] &nbsp;&nbsp;  b："1|2|3|4|5"
  </li>
  <li>
    <h4>reverse：将数组反序 </h4>
    var a = [1,2,3,4,5]; <br/>
    var b = a.reverse();&nbsp;&nbsp; //a：[5,4,3,2,1] &nbsp;&nbsp;  b：[5,4,3,2,1]  
  </li>
  <li>
    <h4>map(function)：迭代数组中的每一个元素，并根据回调函数来处理每一个元素，最后返回一个新数组</h4>
    var a = [1,2,3,4,5];<br/>
    var b = a.map(function(val){return val * 4;}); &nbsp;&nbsp; //a：[1,2,3,4,5] &nbsp;&nbsp;  b：[4,8,12,16,20]  
  </li>
  <li>
    <h4>reduce(function)：用来迭代一个数组，并且把它累积到一个值中 </h4>
    var a = [1,2,3,4,5];<br/>
    var b = a.reduce(function(pre,cur){return pre+cur;}); &nbsp;&nbsp; //a：[1,2,3,4,5] &nbsp;&nbsp;  b：15 
  </li>
  <li>
    <h4>filter(function)：用来迭代一个数组，并且按给出的条件过滤出符合的元素 </h4>
    var a = [1,2,3,4,5];<br/>
    var b = a.filter(function(val){return val==3;}); &nbsp;&nbsp; //a：[1,2,3,4,5] &nbsp;&nbsp;  b：[3] 
  </li>
  <li>
    <h4>sort(function)：按字母顺序或数字顺序对数组中的元素进行排序 </h4>
    var a = [4,2,1,5,3];<br/>
    a.sort(function(n,m){return n-m;}); &nbsp;&nbsp; //a：[1,2,3,4,5] 
  </li>
</ul>

<h2>Caesars Cipher</h2>

    /*
    ROT13函数，实现输入加密字符串，输出解密字符串。
    字母会移位13个位置。由'A' ↔ 'N', 'B' ↔ 'O'，以此类推
    所有的字母都是大写，遇到任何非字母形式的字符(例如：空格，标点符号)跳过。
    */
    function rot13(str) {
        var arr = [];
        for(var i=0;i<str.length;i++){
            arr.push(str.charCodeAt(i));
        }
        function myMap(val) {
            if(val >= 65 && val <= 77){
                return val +13;
            }
            if(val > 77 && val <= 90){
                return val-13;
            }
            return val;
        }
        var newArr = arr.map(myMap);
        var newStr = '';
        for(var j=0;j<newArr.length; j++){
            newStr += String.fromCharCode(newArr[j]);
        }
        return newStr;
    }
    rot13("SERR PBQR PNZC");    // 应该解码为 "FREE CODE CAMP"
    rot13("SERR CVMMN!");   // 应该解码为 "FREE PIZZA!"
    rot13("SERR YBIR?");    // 应该解码为 "FREE LOVE?"
    rot13("GUR DHVPX OEBJA QBT WHZCRQ BIRE GUR YNML SBK.");     // 应该解码为 "THE QUICK BROWN DOG JUMPED OVER THE LAZY FOX."

<h2>sort</h2>

    //排序
    (function () {
        var arr1 = [6,85,9,43,2,36];
        var arr2 = [5,93,66,7,24];
        var arr3 = [66,45,88,6,39,1];
        bubbleSort(arr1);   //冒泡排序
        arrSort(arr2);      //sort排序
        quickSort(arr3);    //快速排序
        console.log(arr1);
        console.log(arr2);
        console.log(quickSort(arr3));
        //冒泡排序
        function bubbleSort(arr) {
            for(var i = 0; i<arr.length-1;i++){
                for(var j = i+1; j<arr.length;j++){
                    var tempI = arr[i];
                    var tempJ = arr[j];
                    if(tempI > tempJ){
                        arr[i] = tempJ;
                        arr[j] = tempI;
                    }
                }
            }
        }
        //sort排序
        function arrSort(arr) {
            return arr.sort(function (a,b) {
                return a-b;
            })
        }
        //快速排序
        function quickSort(arr) {
            if(arr.length <= 1) {return arr;}
            var index = Math.floor(arr.length/2);
            var cur = arr.splice(index,1);
            var left = [];
            var right = [];
            for( var i=0;i<arr.length;i++){
                cur > arr[i] ? left.push(arr[i]) : right.push(arr[i]);
            }
            return quickSort(left).concat([cur],quickSort(right));
        }
    })();
