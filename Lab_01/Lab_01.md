# ITI Labs : [Lab 01 ](https://drive.google.com/file/d/1FAo3KbqsqRK1p54LpjCC_IsYeiku3pyO/view?usp=share_link)

## Content 
* [**Objectives**]()
*  [**Part I**](#part-1--lpf)
    * LPF
*  [**Part II**]() 
    * MOS Characteristic   

-----------------------

## Objectives 

* In Part 1 you will
    * Get familiar with Cadence custom IC design tools (Virtuoso Environment).
    * Learn the different types of simulations (transient, ac, pole-zero).
    * Learn how to run parametric sweeps.
* In Part 2 you will
    * Learn the difference between DC and parametric sweeps.
    * Compare the behavior of PMOS and NMOS transistors.
    * Compare the behavior of short-channel and long-channel MOSFETs.

--------------------------

## Part 1 : LPF 

* [**Transient Analysis**]()
* [**AC Analysis**]()

### Transient Analysis

.... picture 1 


* Comment on the results part 1 parametric sweep 
    * Tp = 20ns , PulseWidth = 10 ns
    * |R|C|Time Constant|5 * Time Constant |
      |-|-|-------------|-----------------|
      |1k|1p|1ns|5ns|
      |2k|1p|2ns|10ns|
      |3k|1p|3ns|15ns|
      |4k|1p|4ns|20ns|
      |5k|1p|5ns|25ns|
        
    * The values which greater than 10ns (PusleWidth) won't fall and rise completely

### AC Analysis


|R|Hand Analysis fc|Simulation fc|
|-|----------------|-------------|
|1k|159.15MHz|158.8MHZ|
|10k|15.9MHz|15.88MHZ|
|100k|1.59MHz|1.588MHZ|
|1000k|159.15kHz|158.8kHZ|



## Part 2 : MOS Characteristic

* [ID, gm,ro vs VGS]()
* [ID, gm,ro vs VDS]()


### ID, gm,ro vs VGS

 **Graphs**

* Comment on the differences between short channel and long channel results.
    * Which one has higher current? Why? 
        * Long channel ,as quadratic equation and the another is linear
    * Is the relation linear or quadratic? Why?
        *   Quadratic
* Comment on the differences between NMOS and PMOS.
    * Which one has higher current? Why?
        * NMOS as higher mobility (Mn)
    * What is the ratio between NMOS and PMOS currents at VGS = VDD?
        * 4.8 (long), 3.24(short)
    * Which one is more affected by short channel effects?
        * NMOS is more affected (**Why?**)
* (gm vs VGS) Comment on the differences between short channel and long channel results.
    * Does 𝑔𝑚 increase linearly? Why?
        * As gm proportional to Vov (Vgs)
    * Does 𝑔𝑚 saturate? Why?
        * As in short channel the square law becomes linear and its derivitive is Constant ( but in Long channel doesn't saturate, gm = f(Vov or VGS) linearly)
### ID, gm,ro vs VDS

 **Graphs**

* (ID vs VDS)Comment on the differences between short channel and long channel results.
    * Which one has higher current? Why?
        * Long Channel is higher as ID relation is Quadratic and short channel is Linear
    * Which one has higher slope in the saturation region? Why?
        * Long Channel has higher slope (**WHY?!**)

* Comment on the variation of (𝑔𝑚 vs 𝑉𝐷𝑆).
    * In the first part of the curve, is the relation linear? Why?
        * as in triode the ID =  f(VDS^2)
    * Does 𝑔𝑚 saturate? Why?
        * as in saturation ID = f(VDS) and it's derivitive is constant
    * Where do you want to operate the transistor for analog amplifier applications? Why?
        * We need to operate AMP in saturation as gm almost constant so good linearity

* Comment on the variation of (𝑔𝑚 vs 𝑉𝐷𝑆).
    * Does 𝑟𝑜 saturate just after the transistor enters saturation similar to gm? Why? 
        * saturate as gm in long channel , in short channel decreases (**WHY?!**)(in short channel the ro strong function in VDS)
    * Does 𝑟𝑜 increase if the transistor is biased more into saturation? 
        * No
    * Should we operate the transistor at the edge of saturation? 
        * Yes, high ro and doesn't consume the headroom 
    * Where do you want to operate the transistor for analog amplifier applications? Why?
        * At the edge or a little deeper into saturation. to get high ro to get high gain, and if operates deeper into saturation won't get higher ro and the MOS will consumes the voltage swing !






