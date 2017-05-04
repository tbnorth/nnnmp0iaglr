## Nested Nearshore Nutrient Model (N<sup>3</sup>M)

### Terry Brown, James Pauer,<br/>Tom Hollenhorst<br/>USEPA MED

<http://tbnorth.github.io/nnnmp0iaglr>



# Goals

 - Look at movement of nutrients in near shore
 - Examine influence on algal blooms (large scale / 
   long term)
 - Look at impacts of landuse decisions



<!-- .slide: data-background-video="img/0001-0500.mp4" -->
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



## Implementation

 - Originally in MatLab, now in Python
 - Uses `multiprocessing` (true parallelism) for agents, flow,
   and reading inputs
 - Not a great boost with current test grid, but should help with
   larger grids


### Persistent multi-processing

 - `threading` `Queue` can be `joined()` to wait for all tasks
 - `multiprocessing` `Queue` cannot, a `Pool` must be closed before joining
 - workers far too expensive to start every iteration
 - use two `Queue`s, one to deliver tasks, and one to ping back when a task
   completes



# Results



## Visualization

 - Uses CesiumJS, an in-browser accelrated graphics (WebGL) framework.

