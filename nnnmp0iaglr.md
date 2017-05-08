## Nested Nearshore Nutrient Model (N<sup>3</sup>M)

### Terry Brown, James Pauer,<br/>Tom Hollenhorst<br/>USEPA MED

<http://tbnorth.github.io/nnnmp0iaglr>



# Goals

 - Look at movement of nutrients in near shore
 - Examine influence on algal blooms (large scale / 
   long term)
 - Look at impacts of landuse decisions



<!-- .slide: data-background-video="img/0001-0020.ogv" -->
<!-- .slide: data-background-size="contain" -->
<!-- .slide: data-background-repeat="no-repeat" -->
<!-- .slide: data-background-position="center center" -->













<!-- .slide: data-background="img/21Mar2017Sentinel.png" -->
<!-- .slide: data-background-size="contain" -->
<!-- .slide: data-background-repeat="no-repeat" -->
<!-- .slide: data-background-position="center center" -->



<!-- .slide: data-background="img/map_obs_flat2.png" -->
<!-- .slide: data-background-size="contain" -->
<!-- .slide: data-background-repeat="no-repeat" -->
<!-- .slide: data-background-position="center center" -->



# Model

$V_j\frac{dC_j}{dt} = \sum^n_iQ_i{}_jC_i{}_j + \sum^n_iR_i{}_j(C_i-C_j)+W_j-S_j$



## Implementation

 - Originally in MatLab, now in Python
 - Hybrid cell / agent model
 - Uses `multiprocessing` (true parallelism) for agents, flow,
   and reading inputs
     - Not a great boost with current test grid, but should help with
       larger grids


### Persistent multi-processing

 - `threading` `Queue` can be `joined()` to wait for all tasks to complete
 - `multiprocessing` `Queue` cannot, and a `Pool` must be closed before joining
 - workers far too expensive to start every iteration
 - use two `Queue`s, one to deliver tasks, and one to ping back when a task
   completes



# Results



## Visualization

 - Uses CesiumJS, an in-browser accelrated graphics (WebGL) framework.



