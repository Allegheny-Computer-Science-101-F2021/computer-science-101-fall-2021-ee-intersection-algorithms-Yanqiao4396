# Intersection Algorithms
A project with helps of professor
## Ideas
This project is to figure out the time complexity of tuple, list, doulbe for loop(which means a loop in another for loop), and the combination of for loop and if statment. To dect the time consumption, I used profiler method. Finally, I found that I find that the listsingle
is the fastest one and the tupledouble is the slowest one. And I want to explain it below
in 2 aspects, tuple and list, and double and single.

For the difference between tuple and list, the most prominent one is that tuple is immutable and
list is mutable. This divergence results in the situation that list has the method `append` to add objects or 
values into the end of the initial list, which is a feature that tuple doesn't have.
Instead, what tuple can do to `add` something in it is by the way of using `+=` operator .
And the nature of this operator is actually replace the initial tuple and add a new element into the new one which uses
the same assignment name. The result of this approach is the fact that everytime you want to `add` a new element,
you'd have to cover the elements in the initial again. For this reason, the project can be huge and time-consuming
when there are hundards of elements in the initial tuple.

To figure out the difference between single for loop and double for loop, I'd like to use some concepts about time complexity.
single for loop is totally a  linear function. The relationship between double for loop and time consumption, however, is a quartic
function. So the degree of increasement of time consumption can be so prominent. 

## Output
```
🔬 Here's profiling data from computing an intersection with random data containers of 1000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:28:45  Samples:  2
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.003     CPU time: 0.003
/   _/                      v4.0.3

Program: intersection --number 1000 --maximum 250 --profile --approach ListSingle

0.002 intersection  intersection/main.py:119
└─ 0.002 compute_intersection_list_single  intersection/main.py:80

```

```
🔬 Here's profiling data from computing an intersection with random data containers of 2000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:43:00  Samples:  82
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.083     CPU time: 0.083
/   _/                      v4.0.3

Program: intersection --number 2000 --maximum 100 --profile --approach ListDouble

0.082 intersection  intersection/main.py:119
└─ 0.082 compute_intersection_list_double  intersection/main.py:64
   ├─ 0.079 [self]  
   └─ 0.003 list.append  <built-in>:0
         [2 frames hidden]  <built-in>
```

Run 1: ListDouble with a small input
Run 2: ListDouble with a large input
```
🔬 Here's profiling data from computing an intersection with random data containers of 1000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:29:26  Samples:  21
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.022     CPU time: 0.021
/   _/                      v4.0.3

Program: intersection --number 1000 --maximum 250 --profile --approach ListDouble

0.021 intersection  intersection/main.py:119
└─ 0.021 compute_intersection_list_double  intersection/main.py:64

```
```
🔬 Here's profiling data from computing an intersection with random data containers of 2000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:43:00  Samples:  82
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.083     CPU time: 0.083
/   _/                      v4.0.3

Program: intersection --number 2000 --maximum 100 --profile --approach ListDouble

0.082 intersection  intersection/main.py:119
└─ 0.082 compute_intersection_list_double  intersection/main.py:64
   ├─ 0.079 [self]  
   └─ 0.003 list.append  <built-in>:0
         [2 frames hidden]  <built-in>
```


Run 1: TupleSingle with a small input
Run 2: TupleSingle with a large input
```
🔬 Here's profiling data from computing an intersection with random data containers of 1000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:30:04  Samples:  1
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.003     CPU time: 0.003
/   _/                      v4.0.3

Program: intersection --number 1000 --maximum 250 --profile --approach TupleSingle

0.003 intersection  intersection/main.py:119
└─ 0.003 compute_intersection_tuple_single  intersection/main.py:108
```
```

🔬 Here's profiling data from computing an intersection with random data containers of 2000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:42:13  Samples:  1
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.005     CPU time: 0.005
/   _/                      v4.0.3

Program: intersection --number 2000 --maximum 100 --profile --approach TupleSingle

0.005 intersection  intersection/main.py:119
└─ 0.005 compute_intersection_tuple_single  intersection/main.py:108
```

: Summary of the runs for the ListDouble algorithm:
Run 1: ListDouble with a small input
Run 2: ListDouble with a large input
```
🔬 Here's profiling data from computing an intersection with random data containers of 1000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:30:50  Samples:  1
 /_//_/// /_\ / //_// / //_'/ //     Duration: 0.031     CPU time: 0.031
/   _/                      v4.0.3

Program: intersection --number 1000 --maximum 250 --profile --approach TupleDouble

0.031 intersection  intersection/main.py:119
└─ 0.031 compute_intersection_tuple_double  intersection/main.py:96
```
```
🔬 Here's profiling data from computing an intersection with random data containers of 2000!

  _     ._   __/__   _ _  _  _ _/_   Recorded: 16:39:44  Samples:  1
 /_//_/// /_\ / //_// / //_'/ //     Duration: 1.702     CPU time: 1.702
/   _/                      v4.0.3

Program: intersection --number 2000 --maximum 100 --profile --approach TupleDouble

1.702 intersection  intersection/main.py:119
└─ 1.702 compute_intersection_tuple_double  intersection/main.py:96
```