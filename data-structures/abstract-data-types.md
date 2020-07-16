# Queue and Stack

### Queue: first in first out \(FIFO\)

Java has a `Queue` interface which we can instantiate a concrete implementation. 

```
Queue queueA = new LinkedList(); 
      
Queue queueB = new PriorityQueue();
Queue<MyObject> queue = new LinkedList<MyObject>();
//----------  Summary of Queue methods  ------------//
╒═════════╤══════════════════╤═══════════════════════╕
│         │ Throws exception │ Returns special value │
╞═════════╪══════════════════╪═══════════════════════╡
│ Insert  │ add(e)           │ offer(e)              │
├─────────┼──────────────────┼───────────────────────┤
│ Remove  │ remove()         │ poll()                │
├─────────┼──────────────────┼───────────────────────┤
│ Examine │ element()        │ peek()                │
╘═════════╧══════════════════╧═══════════════════════╛
```



`Deque` interface is a double ended queue.

```text
Deque dequeA = new LinkedList();
Deque dequeB = new ArrayDeque();
Deque<MyObject> deque = new LinkedList<MyObject>();

//-----------------  Summary of Deque methods  -----------------//
╒═╤═══════════════════════════════╤══════════════════════════════╕
│ │ First Element (Head)          │ Last Element (Tail)          │
╞═╪═══════════════╤═══════════════╪══════════════╤═══════════════╡
│ │ Throws exc    │ Special value │ Throws exc   │ Special value │
├─┼───────────────┼───────────────┼──────────────┼───────────────┤
│ │ addFirst(e)   │ offerFirst(e) │ addLast(e)   │ offerLast(e)  │
├─┼───────────────┼───────────────┼──────────────┼───────────────┤
│ │ removeFirst() │ pollFirst()   │ removeLast() │ pollLast()    │
├─┼───────────────┼───────────────┼──────────────┼───────────────┤
│ │ getFirst()    │ peekFirst()   │ getLast()    │ peekLast()    │
╘═╧═══════════════╧═══════════════╧══════════════╧═══════════════╛
```



#### Queue vs Deque

```text
//Equivalent Deque and Queue methods 
╔═╤══════════════╤═══════════════╗
║ │ Queue Method │ Deque Method  ║
╠═╪══════════════╪═══════════════╣
║ │ add(e)       │ addLast(e)    ║
╟─┼──────────────┼───────────────╢
║ │ offer(e)     │ offerLast(e)  ║
╟─┼──────────────┼───────────────╢
║ │ remove()     │ removeFirst() ║
╟─┼──────────────┼───────────────╢
║ │ poll()       │ pollFirst()   ║
╟─┼──────────────┼───────────────╢
║ │ element()    │ getFirst()    ║
╟─┼──────────────┼───────────────╢
║ │ peek()       │ peekFirst()   ║
╚═╧══════════════╧═══════════════╝
```

### 

### Stack: first in last out \(FILO\)

Java has a `Stack` class, which implements `Iterable<E>`, `Serializable`, `Collection<E>`, `List<E>`, `RandomAccess`, `Cloneable` interfaces. 

```text
Stack<String> stack = new Stack<>();
empty()
peek()
pop()
push(E item)
search(Object o)
```



A more consistent and way to implement stack in java is to use `Deque` interface and its implementation. 

```text
Deque<Integer> stack = new ArrayDeque<Integer>();
// Equivalent Deque and Stack methods
╔══════════════╤═══════════════╗
║ Stack Method │ Deque Method  ║
╠══════════════╪═══════════════╣
║ push(e)      │ addFirst(e)   ║
╟──────────────┼───────────────╢
║ pop()        │ removeFirst() ║
╟──────────────┼───────────────╢
║ peek()       │ peekFirst()   ║
╚══════════════╧═══════════════╝
```

