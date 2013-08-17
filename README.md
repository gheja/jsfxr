jsfxr
=====

as3fxr (http://code.google.com/p/as3sfxr/) synth port to JavaScript created for js13kGames

Current version contains various performance/browser compatibility improvements by [@maettig](https://twitter.com/maettig)

New minified size is 2797 bytes (Closure with Advanced Mode, was 3169 bytes) thanks to improvements by [@chandlerprall](https://github.com/chandlerprall). 

Pull requests for further improvements are welcome ;)

Tested with FF 14, Chrome 21 and Opera 12

Usage
=====

1. Create a sound with as3sfxr (http://www.superflashbros.net/as3sfxr/)
2. Copy settings string (Just use Ctrl+C on the as3fxr page) and save it as a JavaScript array 
  * String looks something like this: "0,,0.1812,,0.1349,0.4524,,0.2365,,,,,,0.0819,,,,,1,,,,,0.5"
  * Should be passed as JavaScript array like this: [0,,0.1812,,0.1349,0.4524,,0.2365,,,,,,0.0819,,,,,1,,,,,0.5]
3. Play sound in JS using the following code:

```javascript  
 // asfxr string gets passed into jsfxr as array
 var soundURL = jsfxr([0,,0.1812,,0.1349,0.4524,,0.2365,,,,,,0.0819,,,,,1,,,,,0.5]); 
 var player = new Audio();
 player.src = soundURL;
 player.play();
```

Check out demo.html for some examples. Interactive demo is also available as [jsFiddle](http://jsfiddle.net/mneubrand/tsC8j/6/)
