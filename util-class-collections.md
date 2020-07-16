---
description: java.util.Collections
---

# Util Class: Collections

* Add elements all at once.

```text
// addAll​(Collection<? super T> c, T... elements)
List fruits = new ArrayList(); 
Collections.addAll(fruits, "Apples", "Oranges", "Banana");
```

* Sort

```text
// sort​(List<T> list, Comparator<? super T> c)
// sort list in natural order or customized order
```

* Binary Search. 

The list should be sorted before calling this method. 

```text
// binarySearch​(List<? extends Comparable<? super T>> list, T key)
```

* Max or Min

```text
// max​(Collection<? extends T> coll, Comparator<? super T> comp)
// max​(Collection<? extends T> coll)
```

* Frequency

Return the frequency of a specific object.

```text
// frequency​(Collection<?> c, Object o)
```

* Index of a target subarray

```text
// indexOfSubList​(List<?> source, List<?> target)
// lastIndexOfSubList​(List<?> source, List<?> target)
```

* Replace 

```text
// replaceAll​(List<T> list, T oldVal, T newVal)
```

* Copy

```text
// copy​(List<? super T> dest, List<? extends T> src)
```

* Disjoint

```text
// disjoint​(Collection<?> c1, Collection<?> c2)
// Returns true if the two specified collections have no elements in common.
```

* Others

```text
void reverse(List list)             //反转
void shuffle(List list)             //随机排序
void swap(List list, int i , int j) //交换两个索引位置的元素
void rotate(List list, int distance)//when distance > 0，将list后distance个元素整体移到前面。
```

####  

