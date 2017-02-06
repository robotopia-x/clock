# clock

util to handle dynamic time intervals

```
npm install @robotopia/clock
```

## Usage

### Clock

Clock can be used as a replacement for setInterval. It repeatedly calls a function or executes a code snippet, with a specified time delay between each call. Unlike setInterval the interval can be dynamically changed or paused

```JavaScript
const Clock = require('clock')

const clock = new Clock(300)

// starts clock, will trigger on progress immediately
clock.start()

// tick, called every 300 ms
clock.onTick(() => console.log('tick')) 

// called on requestAnimationFrame in between ticks, progress represents percentage of time passed until next frame
clock.onProgress((progress) => console.log(progress))
 
// stop clock interval 
clock.stop()

```

### Timer

Timer is a replacement for Date.now() with the added ability to pause time

```JavaScript
const Timer = require('clock/timer')

const timer = new Timer()

// starts timer
timer.start()

// returns timestamp relative to when start was called
timer.now()

// pauses clock 
clock.pause()

```

## License

MIT
