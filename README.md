# Quiz-8
*--This is Quiz 8 for Week 9.*

## Part 1: Imaging Technique Inspiration
##### Inspired by audio visualisation technology, I chose two examples of pickups. This artefact visualises invisible audio signals by capturing sound and transforming it into dynamic visual elements. This technique matches the requirement to animate my work using audio track frequencies. Simulating this corresponding effect in p5.js enhances the user interaction experience and explores the connection between sound and vision. 

![**An image of the pickup1**](images/1.png)
##### The first image is a traditional audio equaliser bar graph, with different heights representing different volume frequencies. 

![**An image of the pickup1**](images/1.png)
##### The second graph is an RGB analogue glow tube, presenting audio frequencies in vertical columns of light emanating from the middle to the sides.


## Part 2: Coding Technique Exploration

##### The linear waveform 2 on [this](https://github.com/Ronik22/Audio-Visualizer) website is very similar to the inspiration I mentioned in the first part. Its source code contains two main functions.

### 1. Audio analysis
```
function setup() {
    createCanvas(windowWidth, windowHeight);
    fft = new p5.FFT(0.9)
    ...}
```
##### p5.FFT() analyze the audio.

```
function draw() {
    background(10)
    var wave = fft.waveform()
    var spectrum = fft.analyze()
    ...}
```

##### fft.analyze() breaks down audio into different frequency amplitudes.
##### fft.waveform() obtains the waveform data of the audio.


### 2、visual presentation
```
     if(i%4) {
                y = map(amp, 0, 1024, height, 0) * 1.05
            }
            else if(i%9) {
                y = map(amp, 0, 1024, height, 0) * 1.07
            }
            else if(i%7) {
                y = map(amp, 0, 1024, height, 0) * 1.09
            }
```
##### map() maps the amplitude to the height of the canvas.



