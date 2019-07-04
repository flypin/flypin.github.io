javascript'''
// ==UserScript==
// @name         New Userscript
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  try to take over the world!
// @author       You
// @match        http://epub.sipo.gov.cn/patentoutline.action
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    var title = document.querySelectorAll('td');
    var v='';
    for (var i=0; i<title.length; i++){
      if(title[i].innerHTML.indexOf('javascript')>0 && title[i].innerHTML.indexOf('table')==-1){
          v += title[i].querySelector('a').innerHTML+',';
      }
      if(i>0 && i%4==0)v+='\n';

    }
    alert(v);

    // Your code here...
})();

'''
