# JavaScript framework for the Emotiv EPOC [Work in progress]

This framework provides an interface to access data from the Emotiv EPOC brain sensor using Node.js.

To use this framework, you're gonna need an EPOC or EPOC+ that you can buy [here](https://emotiv.com/). 

## How to Install

In your terminal, run:

```
  npm install epocjs
```


## How to Use

Example of simple program:

```
  var Epoc = require('epocjs')();

  Epoc.connect(function(event){
    if(event.smile > 0){
      console.log('smiling')
    }
  })
```

## Events

---

#### Smile

If the value is superior to 0, the headset is detecting that the user is smiling.

```
  if(event.smile > 0){
    // do something
  }
```

---

#### Looking Up / Down / Left / Right

The headset can detect the direction in which the user is looking:

```
  if(event.lookingUp > 0){
    // do something
  }

  if(event.lookingDown > 0){
    // do something
  }

  if(event.lookingLeft > 0){
    // do something
  }

  if(event.lookingRight > 0){
    // do something
  }
```

---

#### Blink

Detect if the user blinked:

```
  if(event.blink > 0){
    // do something
  }
```

---

#### Winking Left / Right

The headset can detect if the user is winking:

```
  if(event.winkingLeft > 0){
    // do something
  }

  if(event.winkingRight > 0){
    // do something
  }
```

---

#### Laugh

Detect if the user is laughing:

```
  if(event.laugh > 0){
    // do something
  }
```

---

## Next steps

* Add Gyroscope tracking
* Add cognitive tracking of actions like pulling, pushing, etc...

## Special Thanks

Thanks to [Cam Swords](https://github.com/camswords) for his help :)

## License

Licensed under the MIT license.

*Using the [EpocUtils program](https://github.com/stephaneAG/epocutils).
