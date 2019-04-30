# EVA
Assignment :1B

1.What are Channels and Kernels (according to EVA)?

Ans:


    Channel are bag of similar features.So objects that have similar features fall under one channel. If we are asked to divide 
    some balls into three baskets where each basket has a feature like color of balls it can hold. 
    Eg: Basket A will have only red balls, basket B will have only blue balls and basket C will have only green balls. 
    So each basket here represents a channel which has a particular feature which is its color. 


    We can easliy distinguish these balls into different basket on the basis of its color(feature). Distinguishing objects 
    on the basis of its features is done by kernel. So here since we are dividing the balls into different channels(baskets) ,
    we play the role of the kernel.Kernels are also called feature extractor as the kernels make it possible to highlight a 
    particular feature which helps in forming the channels.


2.Why should we only (well mostly) use 3x3 Kernels?

Ans:

There are two arguments to justify the usage of 3*3 kernels:
    
    a. Over even kernels like 2x2
    
      -- 
    
    b.Over odd kernels of higher number like 5*5 or 7*7 etc
     
     --The most important perferring 3x3 matrix and not any other higher odd number matrix as a kernel is lower number 
     of parameters obtained after every operation. 
     
     For instance to obtain 1x1 from a 11x11 image , we will need to perform 5 3x3 convolution operations. 
     Total number of parameters involved will be
        5x9 = 45.
     
     Whereas if we take a higher matrix like 11x11,the number of parameters involved will be 11x11 = 121. 
        Due to this large difference in the number of parameters we have to deal with a smaller matrix 3x3 is preferrable.



3.How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)?

Ans:We have to perform 99 convolution operations to get 1x1 matrix from 199x199.

  Calculation  Here it comes.......

    199x199-> 197x197-> 195x195-> 193x193-> 191x191-> 189x189-> 187x187-> 185x185-> 183x183-> 181x181-> 179x179-> 177x177-> 175x175-> 173x173->
    171x171-> 169x169-> 167x167-> 165x165-> 163x163-> 161x161-> 159x159-> 157x157-> 155x155-> 153x153-> 151x151-> 149x149-> 147x147-> 145x145->
    143x143-> 141x141-> 139x139-> 137x137-> 135x135-> 133x133-> 131x131-> 129x129-> 127x127-> 125x125-> 123x123-> 121x121-> 119x119-> 117x117-> 
    115x115-> 113x113-> 111x111-> 109x109-> 107x107-> 105x105-> 103x103-> 101x101-> 99x99-> 97x97-> 95x95-> 93x93-> 91x91-> 89x89-> 87x87-> 
    85x85-> 83x83-> 81x81-> 79x79-> 77x77-> 75x75-> 73x73-> 71x71-> 69x69-> 67x67-> 65x65-> 63x63-> 61x61-> 59x59-> 57x57-> 55x55-> 53x53-> 
    51x51-> 49x49-> 47x47-> 45x45-> 43x43-> 41x41-> 39x39-> 37x37-> 35x35-> 33x33-> 31x31-> 29x29-> 27x27-> 25x25-> 23x23-> 21x21-> 19x19->
    17x17-> 15x15-> 13x13-> 11x11-> 9x9-> 7x7-> 5x5-> 3x3-> 1x1
