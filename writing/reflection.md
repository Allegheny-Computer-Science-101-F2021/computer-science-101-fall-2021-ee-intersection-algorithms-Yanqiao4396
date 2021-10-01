# Intersection Algorithms

## Yanqiao Chen

## Program Output

### Use eight fenced code blocks to provide output from eight different runs of `intersection` with different inputs

: Summary of the runs for the List-based algorithms:

: Summary of the runs for the ListSingle algorithm:
Run 1: ListSingle with a small input
Run 2: ListSingle with a large input
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
: Summary of the runs for the ListDouble algorithm:
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

: Summary of the runs for the Tuple-based algorithms:

: Summary of the runs for the TupleSingle algorithm:
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

: Whenever possible, please use the same "small" and "large" inputs for both
the List-based and Tuple-based algorithms.

: Do not run the program with the `--display` option when conducting
experiments!

: Document and justify your choice for the `number` and `maximum` variables.

#### Two outputs from running the `ListSingle` algorithm with different inputs

#### Two outputs from running the `ListDouble` algorithm with different inputs

#### Two outputs from running the `TupleSingle` algorithm with different inputs

#### Two outputs from running the `TupleDouble` algorithm with different inputs

## Performance Analysis

: Provide three paragraphs that explain which algorithm is fastest, by how
much it is faster, and how you knew that the it was faster, referencing the data
in the aforementioned command outputs to support your response. You should make
sure that you answer the following research questions:

- RQ: Is intersection faster with a list or a tuple?
- RQ: Is intersection faster with a double-for-loop or a single-for-loop?
- RQ: Overall, what is the fastest approach for computing the intersection?

: Make sure that your responses explain WHY certain algorithms are faster!
: It is not sufficient to only explain WHICH algorithm is faster!

Based on my experience and outcomes got from the program, I find that the listsingle
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
## Source Code

### Describe in detail how the completed source code works

#### A class that defines the four algorithmic options for running the experiment
```
class IntersectionApproach(str, Enum):
    """Define the name for the approach for performing intersection of structured types."""

    list_single = "ListSingle"
    tuple_single = "TupleSingle"
    list_double = "ListDouble"
    tuple_double = "TupleDouble"
```

The class bind each string to a varible.
: Use a fenced code block to provide the requested source code
: Write at least one paragraph to explain the request source code

#### A function signature that defines the command-line interface for `intersection`
```
@cli.command()
def intersection(
    number: int = typer.Option(5),
    maximum: int = typer.Option(25),
    profile: bool = typer.Option(False),
    display: bool = typer.Option(False),
    approach: IntersectionApproach = IntersectionApproach.tuple_single,
) -> None:
```
The first parameter assigns typer.Option(5) into the variable number and gives the variable a limit that it can only contain
integer.
The other ones do the similar things.

: Use a fenced code block to provide the requested source code
: Write at least one paragraph to explain the request source code
: Explain each of the command-line arguments for this program

#### A function that can generate a data container with random values in it
```
def generate_random_container(
    size: int, maximum: int, make_tuple: bool = False
) -> Union[List[int], Tuple[int, ...]]:
    """Generate a random list defined by the size and with no number bigger than maximum."""
    random_list = []
    for _ in range(size):
        random_list.append(random.randint(0, maximum))
    if make_tuple is True:
        tuple_random = ()
        for values in random_list:
            tuple_random += (values,)
        return tuple_random
    return random_list
```
This function generates a list or a tuple ( based on the requirements) to contain certain numbers of random values.
I used append method to add values into the list and += operator to add values into the tuple.
: Use a fenced code block to provide the requested source code
: Write at least one paragraph to explain the request source code
: Explain each line of source code in this function

### What was the greatest challenge that you faced when completing this assignment?
The greatest challenge I met is how to get a relatively big enough outcome. Just because the TupleDouble is too slow,
when I found a input which can make others' time consumptions moderately big, the TupleDouble took more than 5 minutes
to output results.
: Provide a one-paragraph response that answers this question in your own words.

### Leveraging your response to the previous question, how did you overcome the challenge?
I asked professor Kap and he told me that I don't need meet that severe requirements seriously. So I noticed that. what I already had was good enough.
: Provide a one-paragraph response that answers this question in your own words.
