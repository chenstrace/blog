---
title: js的eval
tags:
  - js 
  - eval 
categories:
  - js 
date: 2016-01-26 11:48:35
---

## Source
    var str1 = "{age:    24}";
    var res1 = eval(str1);
    console.log("typeof(res1) is " + typeof(res1));
    console.log(res1);
    
    var str2 = "\"{age:  24}\"";
    var res2 = eval(str2);
    console.log("typeof(res2) is " + typeof(res2));
    console.log(res2);
    
    var str3 = "({age:   24})";
    var res3 =eval(str3);
    console.log("typeof(res3) is " + typeof(res3));
    console.log(res3);
    
## Output
    typeof(res1) is number
    24
    typeof(res2) is string
    {age:  24}
    typeof(res3) is object
    { age: 24 }
