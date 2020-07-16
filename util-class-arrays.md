---
description: java.util.Arrays
---

# Util Class: Arrays

* Sort : `sort()`

```text
Integer[] a = {1, 3, 7, 5, 2, 4, 9};
		
Arrays.sort(a);    // O(n log n) performance
                   
// sort(T[] a, Comparator<? super T> c)
// sort(T[] a, int fromIndex, int toIndex, Comparator<? super T> c)
```

```text
// sort reverse order
Arrays.sort(a, Collections.reverseOrder());
```

* Search : `binarySearch()`

```text
char[] letters = {'a', 'd', 'c', 'f'};
int idx= Arrays.binarySearch(letters, 'c');
```

* Compare: `equals()`

`array1.equals(array2)` will be true only if they are the same instances, i.e. referencing same object.

`Arrays.equals(array1, array2)` will be true if each elements are equal at same indexes. But it will not compare the nested arrays' elements.

```text
int[] array1 = {1, 2, 3};
int[] array2 = {1, 2, 3};
```

```text
boolean equalsA = Arrays.equals(array1, array2);    
// equalsA = true;
boolean equalsB = array1. equals(array2);
// equalsB = false;
```

`Arrays.deepEquals(array1, array2)`: same as `Arrays.equals()`, but it will also check nested arrays recursively.

```text
Object[] array3 = {3, 5, new int[]{6, 7, 9}};
Object[] array4 = {3, 5, new int[]{6, 7, 9}};
```

```text
boolean equalsC = Arrays.equals(array3, array4);      // = false;    
boolean equalsD = Arrays.deepEquals(array3, array4);  // = true;
```

* Fill elements : `fill()`

```text
int[] nums = {1, 2, 4, 5, 6};
Arrays.fill(nums, 3);        // nums = {3, 3, 3, 3, 3};
```

```text
// fill(Object[] a, Object val)
// fill(Object[] a, int fromIndex, int toIndex, Object val)
```

* Convert array to list: `asList()`

```text
List<String> names = Arrays.asList("Larry", "Kelly", "Curry");
```

* Convert content to string : `toString()`

```text
char[] k = { 'a', 'b', 'c', 'd', 'e'};
System.out.println(Arrays.toString(k));   //[a, b, c, d, e]
```

* Copy: `copyOf()`

```text
// copyOf(T[] original, int newLength)
// copyOfRange(T[] original, int from, int to)
```

####  

