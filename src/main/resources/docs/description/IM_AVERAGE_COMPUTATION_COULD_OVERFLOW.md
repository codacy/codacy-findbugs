The code computes the average of two integers using either division or signed right shift, and then uses the result as the index of an array. If the values being averaged are very large, this can overflow (resulting in the computation of a negative average). Assuming that the result is intended to be nonnegative, you can use an unsigned right shift instead. In other words, rather that using (low+high)/2, use (low+high) >>> 1 This bug exists in many earlier implementations of binary search and merge sort. Martin Buchholz found and fixed it in the JDK libraries, and Joshua Bloch widely publicized the bug pattern.