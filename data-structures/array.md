# Array and ArrayList

### Array



A container of elements of the same data type. It is immutable. 

```text
int[] list = new int[]{1, 2, 3};
String[] names = new String[]{"Adam", "Ben", "Charlie"};
int[][] grid = {{1, 2, 3}, {4, 5, 6}};
list[0] = 0;    // change the first element to be 0.

int size = list.length;   // get the size of an array.
```

### ArrayList

ArrayList is an ordered list of values which allows duplicates. The size of an A_rrayList_ can be changed. We can add or remove elements. Properties:

* Random access: `O(1)`
* Add element: `O(1)`
* Insert/Delete: `O(n)`
* Search in unsorted array: `O(n)` ; in sorted array: `O(log n)`

```text
ArrayList<String> list = new ArrayList<>();
Integer[] intArray = {1, 2, 3, 4};
ArrayList<Integer> intList = new ArrayList<>(Arrays.asList(intArray));
list.add("Hello");              // add(E elem);
list.add(1, "world");           // add(int index, E elem);
list.addAll(anotherArrayList);
list.get(1);                    // get(int index);
list.set(1, "end");             // set(int index, E elem);
list.indexOf("Hello");  
list.lastIndexOf("e");
list.remove(1);                 // remove(int index);
list.contains("hello");         // if contains "hello"
int size = list.size();         // get the size of list
```



#### 1. Convert List to Array:

```text
Object[] objects = list.toArray();
//or
String[] objects1 = list.toArray(new String[0]);
```

#### 2. Convert Array to List

```text
String[] values = new String[]{ "one", "two", "three" };

List<String> list = Arrays.asList(values);
List<String> names = Arrays.asList("Larry", "Kelly", "Curry");

int[] ints = {1,2,3};
List<Integer> list = Arrays.stream(ints).boxed().collect(Collectors.toList());
```

#### 3. Sum int array

```text
int [] arr = {1,2,3,4};
int sum = Arrays.stream(arr).sum();    // print: 10

int sum = Arrays.stream(new int []{1,2,3,4}, 0, 2).sum(); 
//print result of (1 + 2) : 3    
```

#### 4. Sort an ArrayList

```text
Collections.sort(ArrayList, Collections.reverseOrder());
// Descending Order with Collections.reverseOrder();

```

