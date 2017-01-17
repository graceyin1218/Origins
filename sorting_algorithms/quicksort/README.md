# Quicksort

#### About

Quicksort is a popular, comparison-based sorting algorithm. It takes on average O(n log n) comparisons to sort n items (worst case is O(n^2)... which will be addressed a bit further down). The fact that it's in-place and (generally) efficient, means it's a common algorithm used to implement default sorting algorithms (for example, Java 7's `Arrays.sort()`). 

It works by picking a pivot that (ideally) splits the unordered list in half, and then separating the list into values smaller than the pivot, and values larger than the pivot (arbitrarily pick one side to put values equal to the pivot). 

Recurse on each partition (continue picking new pivots and partitioning), until partitions are trivial (i.e. length 0 or 1).


#### Origin

Quicksort was created by Brittish computer scientist Tony Hoare in 1959. He was working on a machine translation project for the UK's National Physical Laboratory and had to sort the words in Russian sentences before looking them up in a Russian-English dictionary (which was already sorted in alphabetical order on... [gasp!] magnetic tape!).

After realizing that insertion sort would be too slow, he came up with the idea for Quicksort! However, the language he used - Mercury Autocode - wasn't suited for the job. Hoare could partition, but "couldn't write the program to account for the list of unsorted segments." Then he learned ALGOL, and its recursive abilities allowed him to publish Quicksort in ACM. 

Since then, quicksort had grown tremendously in popularity and has been adopted in many programming languages' libraries. 

---

Now, remember the worst-case time of O(n^2)? This occurs only if the pivots you choose break the array into an array of length 1 and another of length n-1. (Which basically regresses into insertion sort...) 

To avoid such atrocities, much research has been conducted on ideal pivot selection schemes. With the exception of Samplesort, none of them have very appealing names... Hoare's scheme, Lomuto's partition scheme, Yaroslavskiy's quicksort (which is the one Java 7 used).


#### Sources

https://en.wikipedia.org/wiki/Quicksort

https://cs.stanford.edu/people/eroberts/courses/soco/projects/2008-09/tony-hoare/quicksort.html

(eww Stanford :p )

