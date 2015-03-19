M4Tween
===========

Dependencies
------------
None

Example
------------
### Basic
```js
var element = document.getElementById('bouboup');
M4Tween.to(element, 1, {marginLeft:"10px"});
```
### Delay
```js
M4Tween.to(element, 1, {color:"#000000", backgroundColor:"#ffffff", delay:5});
```
### Abstracts Objects
```js
var myObject =
{
	someProp:0,
	someOtherProp:200
};
M4Tween.to(myObject, .7, {useStyle:false, someProp:300, someOtherProp:-300});
```

API Reference
-------------
### M4Tween
#### to(pElement, pDuration, pProperties)
Check tween's pool, instanciate more if necessary, get & setup one before returning it

* pElement (*object*) : M4Tween's target
* pDuration (*number*) : Tween's duration
* pProperties (*object*) : Target's properties to animate & optionnal parameters (delay, useStyle...)

#### killTweensOf(pTarget, pComplete)
Push every tweens of pTarget into a local "Garbage collector" (array of tweens to be cleaned before getting back to the passive pool)

* pTarget (*object*) : Target
* pComplete (*object*) : Indicate whether it trigger "onComplete" callback or not

#### onStart(pCallBack)
Callback to trigger when the tween start (Only when a delay is set)

* pCallBack (*function*) : function to execute

#### onUpdate(pCallBack)
Callback to trigger when the tween is running

* pCallBack (*function*) : function to execute

#### onComplete(pCallBack)
Callback to trigger when the tween is completed

* pCallBack (*function*) : function to execute

#### then(pTarget, pDuration, pProperties)
Setup a new Tween to start once the current one is complete

* pElement (*object*) : M4Tween's target
* pDuration (*number*) : Tween's duration
* pProperties (*object*) : Target's properties to animate & optionnal parameters (delay, useStyle...)