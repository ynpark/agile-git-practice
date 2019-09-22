# Interesting Talk

[This is a talk](
https://www.youtube.com/watch?time_continue=55&v=vfDazZfxlNs) on fused-effects given by Patrick Thomson at Strange Loop. To give a little bit of background:

>fused-effects is an effect system for Haskell emphasizing expressivity and efficiency. 
>The former is achieved by encoding algebraic, higher-order effects, while the latter is 
>the result of fusing effect handlers all the way through computations” (qtd. from [README](https://github.com/fused-effects/fused-effects/blob/master/README.md)). 

Monads (a data structure used to express effects as data) don’t naturally compose, so most people use mtl (monad transformer library) to compose together different kinds of effects. But monad transformers produce a combined effect consisting of statically fixed layers of effects, making them less expressive. What’s interesting about fused-effects (and other effect system implementations, but I only know about this one) is that you get the speed of mtl without any of its expressive drawbacks. Instead of having a monad stack, you have a single monad whose type reflects possible computation values. I’m curious to see more successful use cases of libraries like fused-effects.
