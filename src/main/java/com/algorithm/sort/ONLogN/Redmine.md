快速排序、归并排序、堆排序之间，究竟有什么样的差别呢？

还是先从性能来分析，虽然快速排序的平均时间复杂度是O（nlogn），但是在极端情况下，最坏时间复杂度是O（n^2）。

而归并排序和堆排序的时间复杂度稳定在O（nlogn）。

至于平均时间复杂度，虽然三者同样都是O（nlogn），但是堆排序比前两者的性能略低一些。为什么呢？主要是由于二叉堆的父子节点在内存中并不连续。

在访问内存数据时，对于顺序存储的数据，读写效率往往是最高的。根据CPU的空间局部性原理，CPU在每次访问数据的时候，会把内存中相邻的数据也一并存入缓存。这样一来，CPU以后再访问邻近的数据就不需要重新访问内存，而是访问CPU缓存，从而大大提升了程序执行的效率。


堆排序的平均性能比快速排序和归并排序略低。

至于排序的稳定性，归并排序是稳定排序，快速排序和堆排序是不稳定排序。

此外，快速排序和堆排序是原地排序，不需要开辟额外空间。而归并排序是非原地排序，在merge操作的时候需要借助额外的辅助数组来完成。