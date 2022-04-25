# Collection-in-Java
The Collection in Java is a framework that provides an architecture to store and manipulate the group of objects.

Java Collection means a single unit of objects. Java Collection framework provides many interfaces (Set, List, Queue, Deque) and classes (ArrayList, Vector, LinkedList, PriorityQueue, HashSet, LinkedHashSet, TreeSet).

# Hierarchy of Collection Framework
 ![Array Collection hierarchy](https://user-images.githubusercontent.com/69740695/165027338-7fb38e8c-3158-4d9a-a70f-99687dfee4bb.png)
 
# List Interface
List interface is the child interface of Collection interface. It inhibits a list type data structure in which we can store the ordered collection of objects. It can have duplicate values.
List interface is implemented by the classes ArrayList, LinkedList, Vector, and Stac

## ArrayList
It is a class of List interface and it provide to make a collection of objects [].
It allow duplicate objects and maintain the order insertion.
It store objects in contiguous form.
The ArrayList class is a resizable array, which can be found in the java.util package.
It are more flexible and dynamic in size, as in built-in array size is fixed while declaring it.

example:

#### To declare and add object: 
```
import java.util.ArrayList;

class Main{
  public static void main(String[] args){
    ArrayList<String> arrayName = new ArrayList<String>(); 
    arrayName.add("obj1");
    arrayName.add("obj2);
  }
}
```

```
outPut:
[obj1,obj2]
```

#### To remove objects:
```
arrayName.remove("obj1"); //(object_name)
```

```
outPut:
[obj1]
```
#### To change any objects:
```
arrayName.set(0,"object changed"); //(index,object_name)
```

```
outPut:
[object changed,obj2]
```
#### For clear and size:
```
arrayName.clear(); //clear all objects
arrayName.size(); //to see size

```
```
outPut:
[]
2
```

### For sorting:
```
arrayName.add("jack");
   arrayName.add("john");
   arrayName.add("rupa"
   arrayName.add("anthony");
Collectins.sort(arrayName);
```

```
outPut:
[anthony, jack, john, rupa]

```

## LinkedList;
It is a class of List interface and it provide to make a collection of objects [].
It allow duplicate objects and maintain the order insertion.
Unlike ArrayList, it store objects in node form which contains pointer and address for its next node in memory.
The ArrayList class is a resizable array, which can be found in the java.util package.
It are more flexible and dynamic in size, as in built-in array size is fixed while declaring it.

example:

#### To declare and add object: 
```
import java.util.LinkedList;

class Main{
  public static void main(String[] args){
    LinkedList<String> arrayName = new LinkedList<String>(); 
    arrayName.add("obj1");
    arrayName.add("obj2);
  }
}
```
#### To remove object:
```
arrayName.remove("obj1"); //(object_name) for first object only not all.
```
#### To change any object:
```
arrayName.set(0,"object changed"); //(index,object_name)
```
#### For clear and size:
```
arrayName.clear(); //clear all objects
arrayName.size(); //to see size
```
#### some more:
```
arrayName.addFirst("first") // added to first List
arrayName.addLast("first") // added to Last of List
arrayName.getFirst() // to get First object
arrayName.getLast() // to get Last object
arrayName.removeFirst() // to remove First object
arrayName.removeLast() // to remove Last object
```
## Vector
Vector uses a dynamic array to store the data elements. It is similar to ArrayList. However, It is synchronized and contains many methods that are not the part of Collection framework.
 example:
 ```
 import java.util.Vector;  
public class Main{  
  public static void main(String args[]){  
    Vector<String> v=new Vector<String>();  
      arrayName.add("one");  
      arrayName.add("two");  
      arrayName.add("three");  
      arrayName.add("four");  
    Iterator<String> itr=v.iterator(); // Iterator object for looping through your List.
    while(itr.hasNext()){  
    System.out.println(itr.next());  
    }   
  }  
}  
 ```
 
 ## Stack
The stack is the subclass of Vector. It implements the last-in-first-out data structure, i.e., Stack. The stack contains all of the methods of Vector class and also provides its methods like boolean push(), boolean peek(), boolean push(object o), which defines its properties.
 example:
 ```
 import java.util.Stack;  
public class Main{  
  public static void main(String args[]){  
    Vector<String> v=new Vector<String>();  
      arrayName.add("one");  
      arrayName.add("two");  
      arrayName.add("three");  
      arrayName.add("four");  
    Iterator<String> itr=v.iterator();  
    while(itr.hasNext()){  
    System.out.println(itr.next());  
    }   
  }  
}  
 ```
 
# Queue Interface
Queue interface maintains the first-in-first-out order. It can be defined as an ordered list that is used to hold the elements which are about to be processed. There are various classes like PriorityQueue, Deque, and ArrayDeque which implements the Queue interface.

## PriorityQueue
The PriorityQueue class implements the Queue interface. It holds the elements or objects which are to be processed by their priorities. PriorityQueue doesn't allow null values to be stored in the queue.
Order is not preserved.
Duplicates allowed 


 example:
 ```
 import java.util.PriorityQueue;  
public class Main{  
  public static void main(String args[]){  
    PriorityQueue<String> arrayName=new PriorityQueue<String>();  
      arrayName.add("one");  
      arrayName.add("two");  
      arrayName.add("three");  
      arrayName.add("four");  
    Iterator<String> itr=arrayName.iterator();  
    while(itr.hasNext()){  
    System.out.println(itr.next());  
    }   
  }  
}  
 ```
 #### to remove object/s
 ```
 arrayName.remove("a"); // (object name)
 ```
## Deque Interface
Deque interface extends the Queue interface. In Deque, we can remove and add the elements from both the side. Deque stands for a double-ended queue which enables us to perform the operations at both the ends.
example:
```
Deque d = new ArrayDeque();  
```

## ArrayDeque
ArrayDeque class implements the Deque interface. It facilitates us to use the Deque. Unlike queue, we can add or delete the elements from both the ends.
ArrayDeque is faster than ArrayList and Stack and has no capacity restrictions.
Order is preserved.
Duplicates allowed .

example:
```
import java.util.ArrayDeque;  
public class Main{  
public static void main(String[] args) {  
//Creating Deque and adding elements  
Deque<String> arrayName = new ArrayDeque<String>();  
arrayName.add("one");  
arrayName.add("two");  
arrayName.add("three");  
//Traversing elements  
for (String i : deque) {  
System.out.println(i);  
}  
}  
}  
```

# Set Interface
Set Interface in Java is present in java.util package. It extends the Collection interface. It represents the unordered set of elements which doesn't allow us to store the duplicate items. We can store at most one null value in Set. Set is implemented by HashSet, LinkedHashSet, and TreeSet.

## HashSet
HashSet class implements Set Interface. It represents the collection that uses a hash table for storage. Hashing is used to store the elements in the HashSet. It contains unique items.
and in HashMap however, store items can be store in "key/value" pairs, and you can access them by an index of another type (e.g. a String).

example:
```
import java.util.HashSet;  
public class Main{  
  public static void main(String args[]){  
//Creating HashSet and adding elements  
    HashSet<String,String> arrayName=new HashSet<String,String>();  
    arrayName.put("one","1");  
    arrayName.put("two","2"); 
    arrayName.put("three","3"); 
    arrayName.add("four","4");  
//Traversing elements  
  Iterator<String> itr=arrayName.iterator();  
    while(itr.hasNext()){  
      System.out.println(itr.next());  
    }   
  }  
}  
```
### to access an item and to remmove
```
arrayName.get("one");  //(key name)
arrayName.remove(two"); //(key name)
arrayName.clear(); // to remove all
```
### to loop in hashmap(key/value)
```
for(String i : arrayName.keySet()){
System.out.println(i);
}
```

## LinkedHashSet
LinkedHashSet class represents the LinkedList implementation of Set Interface. It extends the HashSet class and implements Set interface. Like HashSet, It also contains unique elements. It maintains the insertion order and permits null elements.

example:
```
import java.util.LinkedHashSet;  
public class Main{  
  public static void main(String args[]){  
//Creating LinkedHashSet and LinkedHashSet elements  
    HashSet<String> arrayName=new HashSet<String>();  
    arrayName.add("one");  
    arrayName.add("two");  
    arrayName.add("three");  
    arrayName.add("four");  
//Traversing elements  
  Iterator<String> itr=arrayName.iterator();  
    while(itr.hasNext()){  
      System.out.println(itr.next());  
    }   
  }  
}
```
## SortedSet Interface
SortedSet is the alternate of Set interface that provides a total ordering on its elements. The elements of the SortedSet are arranged in the increasing (ascending) order. The SortedSet provides the additional methods that inhibit the natural ordering of the elements.

example:
```
SortedSet<data-type> arrayName = new TreeSet();  
```
## TreeSet
Java TreeSet class implements the Set interface that uses a tree for storage. Like HashSet, TreeSet also contains unique elements. However, the access and retrieval time of TreeSet is quite fast. The elements in TreeSet stored in ascending order.
```
example:
import java.util.TreeSet;  
public class Main{  
  public static void main(String args[]){  
//Creating TreeSet and TreeSet elements  
    HashSet<String> arrayName=new HashSet<String>();  
    arrayName.add("one");  
    arrayName.add("two");  
    arrayName.add("three");  
    arrayName.add("four");  
//Traversing elements  
  Iterator<String> itr=arrayName.iterator();  
    while(itr.hasNext()){  
      System.out.println(itr.next());  
    }   
  }
}
```
