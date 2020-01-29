The description says
> "Jess doesn't get enough sleep, _since he's such a gamer_ so in this challenge, you'll be staying up with him until 4:00 in the morning :D on a Monday! Let's go, gamers!"

The hint gives you link to the website, https://riceteacatpanda.wtf/onlyrealgamers, it has a timer running which means until the end of the event, you wont be able to get the flag. 
On viewing the source of the page (view-source:https://riceteacatpanda.wtf/onlyrealgamers), under the script tag, you find a js code. I personally use https://html-cleaner.com/js/ to get scripts indented properly. The script says 

> var _0x1d8e = ['gamerfuel=Jan\x2027,\x208020\x2004:20:00',
> 'Jan\x2027,\x208020\x2004:20:00', 'getTime', 'exec', 'floor',
> 'getElementById', 'gamer\x20timer', 'AES', 'decrypt',
> 'U2FsdGVkX18kRm6FDkRVQfVuNPTxyOnJzpu8QnI/9UKoCXp6hQcley11nBnLIItj',
> 'ok\x20boomer', 'innerHTML', 'Utf8', 'cookie']; (function(_0x29eed8,
> _0x4bb4aa) {
>     var _0x47e29c = function(_0x2d3fd2) {
>         while (--_0x2d3fd2) {
>             _0x29eed8['push'](_0x29eed8['shift']());
>         }
>     };
>     _0x47e29c(++_0x4bb4aa); }(_0x1d8e, 0x99)); var _0x2ad1 = function(_0x545e19, _0x47cdd3) {
>     _0x545e19 = _0x545e19 - 0x0;
>     var _0x4275c2 = _0x1d8e[_0x545e19];
>     return _0x4275c2; }; document[_0x2ad1('0x0')] = _0x2ad1('0x1'); var countDownDate = new Date(_0x2ad1('0x2'))[_0x2ad1('0x3')](); var x
> = setInterval(function() {
>     var _0x27a8c6 = new Date(/[^=]*$/ [_0x2ad1('0x4')](document[_0x2ad1('0x0')])[0x0])[_0x2ad1('0x3')]();
>     var _0x5b92f1 = new Date()['getTime']();
>     var _0x3a5a33 = _0x27a8c6 - _0x5b92f1;
>     var _0x4214a2 = Math[_0x2ad1('0x5')](_0x3a5a33 / (0x3e8 * 0x3c * 0x3c * 0x18));
>     var _0x48c0d9 = Math[_0x2ad1('0x5')](_0x3a5a33 % (0x3e8 * 0x3c * 0x3c * 0x18) / (0x3e8 * 0x3c * 0x3c));
>     var _0x2de271 = Math[_0x2ad1('0x5')](_0x3a5a33 % (0x3e8 * 0x3c * 0x3c) / (0x3e8 * 0x3c));
>     var _0x240ffb = Math['floor'](_0x3a5a33 % (0x3e8 * 0x3c) / 0x3e8);
>     document[_0x2ad1('0x6')](_0x2ad1('0x7'))['innerHTML'] = _0x4214a2 + 'd\x20' + _0x48c0d9 + 'h\x20' + _0x2de271 + 'm\x20' + _0x240ffb + 's\x20';
>     if (_0x3a5a33 < 0x0) {
>         clearInterval(x);
>         var _0x1018af = CryptoJS[_0x2ad1('0x8')][_0x2ad1('0x9')](_0x2ad1('0xa'),
> _0x2ad1('0xb'));
>         document[_0x2ad1('0x6')](_0x2ad1('0x7'))[_0x2ad1('0xc')] = _0x1018af['toString'](CryptoJS['enc'][_0x2ad1('0xd')]);
>     } }, 0x3e8);

Looks like the function **var 0x_2ad1** picks something from the **var 0x_1d8e** and alters it. I changed the first two entries of the array to an date and time which was 1 minute away. 

Having a offline copy of the html source, change the time and open the offline page on your browser.
Say, you want it to be at Jan29-2020 15:50:00, change it
to       ‘gamerfuel=Jan\x2020,\x200129\x2015:50:00’ (0129 - Jan29)
from   ‘gamerfuel=Jan\x2027,\x208020\x2004:20:00’.
and similarly the other entry.

 It gives you the flag. 
![](https://github.com/TheCodeYoda/RiceTeaCatPandaCTF/blob/master/web/No%20Sleep/Screenshot%20from%202020-01-29%2015-52-07.png)The description says
> "Jess doesn't get enough sleep, _since he's such a gamer_ so in this challenge, you'll be staying up with him until 4:00 in the morning :D on a Monday! Let's go, gamers!"

The hint gives you link to the website, https://riceteacatpanda.wtf/onlyrealgamers, it has a timer running which means until the end of the event, you wont be able to get the flag. 
On viewing the source of the page (view-source:https://riceteacatpanda.wtf/onlyrealgamers), under the script tag, you find a js code. I personally use https://html-cleaner.com/js/ to get scripts indented properly. The script says 

    var _0x1d8e = ['gamerfuel=Jan\x2027,\x208020\x2004:20:00', 'Jan\x2027,\x208020\x2004:20:00', 'getTime', 'exec', 'floor', 'getElementById', 'gamer\x20timer', 'AES', 'decrypt', 'U2FsdGVkX18kRm6FDkRVQfVuNPTxyOnJzpu8QnI/9UKoCXp6hQcley11nBnLIItj', 'ok\x20boomer', 'innerHTML', 'Utf8', 'cookie']; (function(_0x29eed8,
    _0x4bb4aa) {
        var _0x47e29c = function(_0x2d3fd2) {
            while (--_0x2d3fd2) {
                _0x29eed8['push'](_0x29eed8['shift']());
            }
        };
        _0x47e29c(++_0x4bb4aa); }(_0x1d8e, 0x99)); var _0x2ad1 = function(_0x545e19, _0x47cdd3) {
        _0x545e19 = _0x545e19 - 0x0;
        var _0x4275c2 = _0x1d8e[_0x545e19];
        return _0x4275c2; }; document[_0x2ad1('0x0')] = _0x2ad1('0x1'); var countDownDate = new Date(_0x2ad1('0x2'))[_0x2ad1('0x3')](); var x
    = setInterval(function() {
        var _0x27a8c6 = new Date(/[^=]*$/ [_0x2ad1('0x4')](document[_0x2ad1('0x0')])[0x0])[_0x2ad1('0x3')]();
        var _0x5b92f1 = new Date()['getTime']();
        var _0x3a5a33 = _0x27a8c6 - _0x5b92f1;
        var _0x4214a2 = Math[_0x2ad1('0x5')](_0x3a5a33 / (0x3e8 * 0x3c * 0x3c * 0x18));
        var _0x48c0d9 = Math[_0x2ad1('0x5')](_0x3a5a33 % (0x3e8 * 0x3c * 0x3c * 0x18) / (0x3e8 * 0x3c * 0x3c));
        var _0x2de271 = Math[_0x2ad1('0x5')](_0x3a5a33 % (0x3e8 * 0x3c * 0x3c) / (0x3e8 * 0x3c));
        var _0x240ffb = Math['floor'](_0x3a5a33 % (0x3e8 * 0x3c) / 0x3e8);
        document[_0x2ad1('0x6')](_0x2ad1('0x7'))['innerHTML'] = _0x4214a2 + 'd\x20' + _0x48c0d9 + 'h\x20' + _0x2de271 + 'm\x20' + _0x240ffb + 's\x20';
        if (_0x3a5a33 < 0x0) {
            clearInterval(x);
            var _0x1018af = CryptoJS[_0x2ad1('0x8')][_0x2ad1('0x9')](_0x2ad1('0xa'),
    _0x2ad1('0xb'));
            document[_0x2ad1('0x6')](_0x2ad1('0x7'))[_0x2ad1('0xc')] = _0x1018af['toString'](CryptoJS['enc'][_0x2ad1('0xd')]);
        } }, 0x3e8);

Looks like the function **var 0x_2ad1** picks something from the **var 0x_1d8e** and alters it. I changed the first two entries of the array to an date and time which was 1 minute away. 

Having a offline copy of the html source, change the time and open the offline page on your browser.
Say, you want it to be at Jan29-2020 15:50:00, change it
to       ‘gamerfuel=Jan\x2020,\x200129\x2015:50:00’ (0129 - Jan29)
from   ‘gamerfuel=Jan\x2027,\x208020\x2004:20:00’.
and similarly the other entry.

 It gives you the flag. 
![](https://github.com/TheCodeYoda/RiceTeaCatPandaCTF/blob/master/web/No%20Sleep/Screenshot%20from%202020-01-29%2015-52-07.png)
**rtcp{w0w_d1d_u_st4y_up?}**

