# point-grouping-test

A coding challenge for a Platform Engineer.

One of the most enduring technical challenges at MakeSpace involves generating the routes that our vans and trucks run every day. A good routing algorithm has to take a group of points on a map and group them according to how many vans we want to run that day. Your job will be to implement this step.

## Instructions

**Your solution should be presented as a standalone script we can run from command line using different input data files, and obtain corresponding output data files.**

Please include instructions, comments and anything you deem relevant for us to evaluate your solution.

You can submit it as a Github repository or compressed file.

### The main goal: grouping

`points.json` is a JSON data file that contains a list of objects representing geographic points, with a `lat`, `lon` and `id`. Your job is to write a Python script that will take an integer argument *n*, then read the file and output the `id`s of all the points, grouped into *n* groups, into a second file, `groups.json`. That file should be formated as a list of lists with similar dictionnaries to the `points.json` file.

```json
[
  [
   {
      "lat":4.230509857737786,
      "lon":-58.83513917625535,
      "id":"c24e8984-abd3-4e2a-ac5e-0dead05725f8"
   },
   {
      "lat":-15.056322793924458,
      "lon":-52.76070496476228,
      "id":"5403d956-b94b-4e9a-ad19-01b7f1eb9e56"
   }
  ],
  [
   {
      "lat":-56.31197261613533,
      "lon":24.017742442610725,
      "id":"4c399c25-f123-4779-851d-d0596159b898"
   }
  ]
]
```


Given that the data set represents geographic data, you should try to group points by proximity, so that the geographically closest points are grouped together. You should end up with a clean partitioning of the overall space.

### Stretch goal: distribution

When grouping addresses to produce our daily routes, it's important that each van has roughly the same number of stops to make in a day. Do the same as above, with one final optimization - optimize for both geographical proximity, using the function in the first stretch goal, *and* for equal group size for each van.

## About

This repo contains the instructions and template to complete a coding challenge in Python. It is aimed at Python programmers of mid-level experience and up, and is designed to test the programmer's skill in designing and implementing algorithms. 

No external libraries are required—however, due to the algorithmic/numerical nature of the code at hand, Python libraries that provide robust implementations of various mathematical or statistical algorithms might be useful. The programmer should feel free to calibrate their approach to their own experience level. 

Please do not hesitate to ask us any questions before submitting your solution!
