# codeTest
<p> Q1. Write a function that takes a string as input and returns the string reversed. </p>
<pre><code>
  function revers(word){
      var wordArr = word.split('');
      var len = wordArr.length;
      var reveredStr = '';
      for(var i = len-1; i>=0 ; i--){
          reveredStr += wordArr[i];
      }
      return reveredStr ;
    }
    var ans01 = revers('Hello');
    console.log(ans01);
</code></pre>
<br>
<p> Q2. Given a positive integer num, write a function which returns True if num is a perfect square else False. </p>
<pre><code>
  function perfectSquare(num){
    return num > 0 && Math.sqrt(num) % 1 === 0
  }
  var ans02 = perfectSquare(9);
  console.log(ans02);
</code></pre>
<br>
<p>Q3. Given a set of non-overlapping intervals, insert a new interval into the intervals (merge if necessary).</p>
<p>You may assume that the intervals were initially sorted according to their start times. </p>
<br>
<p>Q4. Given a 2D board and a word, find if the word exists in the grid.</p>
<pre><code>
  var board = 
  [ 
    ['A','B','C','E'], 
    ['S','F','C','S'], 
    ['A','D','E','E'] 
  ] 
  function exists(word){
    Array.prototype.concatAll = function() {
        var results = [];
        this.forEach(function(subArray) {
          results.push.apply(results, subArray);
        });
        return results;
    };
    var boardArr = board.concatAll();
    var wordArr = word.split('');
    return wordArr.every(function(wordNum){
        for(var i = 0 ;i <= boardArr.length-1; i++){
            if(wordNum === boardArr[i]) {
              delete boardArr[i];
              return true;
            }
        }
    })
  }
  var ans04 = exists('AASSDD');
  console.log(ans04);
</code></pre>
<br>
<p>Q5. Calculate the sum of two integers a and b, but you are not allowed to use the operator + and </p>
