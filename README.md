## Website Performance Optimization portfolio project


### Summary

The goal of this project is to optimize two given website to realize some certain criteria respectively. With the help of Chrome devTools to identify performance bottlenecks, and improve the performance.

####Part 1: Optimize PageSpeed Insights score for index.html

The modifications are listed as follows:
1. Inlined the JS to load Google fonts, rather than refer to external source.
2. Inlined all CSS to reduce the rendering blocking.
3. Add async attribute to perfmatters.js to avoid blocking.
4. Resize images to fit the mobile device viewport.

####Part 2: Optimize Frames per Second in pizza.html

The modifications are listed as follows:

1. In the function **resizePizzas()**, replaced **document.querySelector()** with **document.getElementById()**, for the second Web API is faster.
2. Re-designed the function **changePizzaSizes()** to avoid redundant operations to speed up the function. Moved the query outside the loop to avoid forced synchronous layout, and replaced **document.querySelectorAll()** with **document.getElementsByClassName()**, which is faster.
3. In the function **updatePositions()**, moved **document.body** from the loop to avoid querying DOM in each iterations. Replaced **document.querySelectorAll()** with **document.getElementsByClassName()**. Declared the phase variable (var phase;) in the initialisation of the for loop to prevent it from being created every time the loop is executed.
4. Changed the number of pizzas generated on page load to be based on the browser window resolution. 
5. Changed the **document.querySelector()** for selecting movingPizzas1 element to **document.getElementById()**, saved it to a local variable called movingPizzas, moved it outside of the for loop, and referenced the movingPizzas variable inside the loop.
