// ==UserScript==
// @name         All TLs
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  try to take over the world!
// @author       You
// @match        https://monitor.trax-cloud.com/d/uPJ9-4CGk/hourly-report-team-leaders?orgId=18*
// @icon         https://www.google.com/s2/favicons?domain=trax-cloud.com
// @require      https://code.jquery.com/jquery-2.1.4.min.js
// @require      https://cdn.jsdelivr.net/jquery.notification/1.0.3/jquery.notification.min.js
// @require      https://raw.githubusercontent.com/kamranahmedse/jquery-toast-plugin/bd761d335919369ed5a27d1899e306df81de44b8/dist/jquery.toast.min.js
// @grant        none
// ==/UserScript==

function injectStylesheet(url) {
    $('head').append('<link rel="stylesheet" href="'+url+'" type="text/css" />');
}

(function() {
    'use strict';
    injectStylesheet("https://cdn.rawgit.com/kamranahmedse/jquery-toast-plugin/bd761d335919369ed5a27d1899e306df81de44b8/dist/jquery.toast.min.css");
     setInterval(function () {
        var Services = $('#panel-94').find('span.panel-title-text').html();
        if (Services.indexOf("Total Productivity") != -1) {
            var pannel = $('#panel-43').find('span.panel-title-text').html();
            if (pannel == undefined) {
                console.log("Hi all");
                setTimeout(function () {
                    document.title=document.querySelector("div:nth-child(3) > div > value-select-dropdown > div > a").innerText;
                    var col= document.querySelector("#panel-153 > div > a").click()
                    col();
                }, 1000 * 2);
                setTimeout(function () {
                    $.toast({
                    heading: 'Tables are ready',
                    icon: 'success',
                    text: 'Team leader id is ' + document.title,
                    bgColor: '#FF1356',
                    textColor: 'white',
                    hideAfter: 5000,
                    stack: 4,
                    position: 'top-left',
                })
                    var tbl= $("#panel-43").find('table');
                    $(tbl).find('tr').each(function(){
                        var currentRow=$(this);
                        currentRow.find("td:eq(1)").remove();
                    });
                    $(tbl).find('thead').remove();

                    var tb2= $("#panel-122").find('table');
                    $(tb2).find('tr').each(function(){
                        var currentRow=$(this);
                        currentRow.find("td:eq(0)").remove();
                    });
                    $(tb2).find('thead').remove();
                }, 1000 * 5);
            }else{
                console.log("running");
            }

        }else{
            console.log("not running");
        }

    }, 1000 * 10);
})();
