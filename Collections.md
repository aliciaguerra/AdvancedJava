Prior to Java 2, Java provided ad hoc classes such as Dictionary, Vector, Stack, and Properties to store and manipulate
groups of objects. Although these classes were quite useful, they have a central, unifying theme. Thus, the way that
you used Vector was different from the way that you used Properties.

The Collections framework was designed to meet several goals.

- The framework had to be high-performance. The implementations for the fundamental Collections (dynamic arrays, linked lists,
  trees, and hashtables) are highly efficient.
- The framework had to allow different types of collections to work in a similar manner and with a high degree of
  interoperability.
- Extending and/or adapting a collection had to be easy.

Towards this end, the entire collections framework is designed around a set of standard interface. Several standard 
implementations such as LinkedList, HashSet, and TreeSet, of these interfaces are provided you use as-is and you may also
implement your own collection, if you choose.

A collections framework is a unified architecture for representing and manipulating collections. All collections 
frameworks contain the following:

- Interfaces: These are abstract data types that represent collections. Interfaces allow collections to be 
  independently of the details of their representation. In object-oriented languages, interfaces generally 
  form a hierarchy.
- Implementations, i.e. Classes: These are concrete implementations of the collection interfaces. In essence,
  they are reusable data structures.
- Algorithms: These are the methods that perform useful computations, such as searching and sorting, on objects
  that implement collection objects. These algorithms are said to be polymorphic: that is, the same method
  can be used on many different implementations of the appropriate collection interface.
  
In addition to collections, the framework defines several map interfaces and collections. Maps store key/value pairs.
Although maps are not collections in the proper use of the term, but they are fully integrated with collections.

<h2>The Collection Interfaces</h2>
The collections framework defines several interfaces. 

- The Collection Interface: This enables you to work with groups of objects; it is at the top of the collections
  hierarchy.
- The List Interface: This extends collection and an instance of List stores ordered collections of elements.
- The Set: This extends collection to handle sets, which must contain unique elements.
- The SortedSet: This extends Set to handle sorted sets.
- The Map: This maps unique keys to values.
- The Map.Entry: This describes an element (a key/value pair) in a map. This is an inner class of a map.
- The SortedMap: This extends map so that they keys are maintained in ascending order.
- The Enumeration: This is a legacy interface and defines the methods by which you can enumerate (obtain
   one at a time) the elements in a collection of objects. The legacy interface has been superceded by
   Iterator.

<h2>The Collection Classes</h2>
Java provides a set of standard collection classes that implement Collection interfaces. Some of the classes
provide full implementations that can be used as-is and others are abstract class, providing skeletal implementations
that are used as starting points.

- AbstractCollection: Implements most of the collection interface
- AbstractList: Extends AbstractCollection and implements most of the list interface.
- AbstractSequentialList: Extneds AbstractList for use by a collection that uses sequential rather than random
  access of its elements.
- LinkedList: Implements a linked list by extending AbstractSequentialList
- ArrayList: Implements a dynamic array by extending AbstractList
- AbstractSet: Extends AbstractCollection and implements most of the Set interface
- HashSet: Extends AbstractSet for use with a hashtable
- LinkedHashSet: Extends HashSet to allow insertion-order operations
- TreeSet: Implements a set stored in a tree. Extends AbstractSet.
- AbstractMap: Extends most of the Map interface.
- HashMap: Extends AbstractMap to use a HashTable.
- TreeMap: Extends AbstractMap to use a tree.
- WeakHashMap: Extends AbstractMap to use a hash table with weak keys.
- LinkedHashMap: Extends hashmap to follow insertion-order operations.
- IdentityMap: Extends AbstractMap and uses reference equality when comparing documents

The AbstractCollection, AbstractSet, AbstractList, AbstractSequentialList, and AbstractMap classes provide skeletal
implementations of the core collection interfaces, to minimize the effort required to implement them.

<h2>The Collection Algorithms</h2>
The Collections framework defines several algorithms that can be applied to collections and maps. These algorithms are
defined as static methods within the Collections class.

Several of the methods can throw a ClassCastException, which occurs when an attempt is made to compare incompatible
types or an UnsupportedOperationException, which occurs when an attempt is made to modify an unmodifiable exception.

Collections defines three static variables: EMPTY_SET, EMPTY_LIST, and EMPTY_MAP. All are immutable.

<h2>How to use an Iterator?</h2>
Often, you will want to cycle through the elements in a collection. For example, you might want to display this
element.

The easiest way to do this is to employ an iterator, which is an object that implements either the iterator or
the ListIterator interface.

Iterator enables you to cycle through a collection, obtaining or removing elements. ListIterator extends iterator
to allow bidirectional traversal of a list and modification of the elements.

<h2>How to Use a Comparator?</h2>
Both TreeMap and TreeSet store elements in sorted order. However, it is the Comparator that defines precisely 
what sorted order means.

This interface lets us sort a given collection any number of different ways. Also the interface can be used to sort 
any instances of any class (even classes we cannot modify).

<h2>Summary</h2>
The Java collections framework gives the programmer access to prepackaged data structures as well as to algorithms for
manipulating them.

A collection is an object that can hold references to other objects. The collection interfaces declare the operations
that can be performed on each type of collection.

The classes and interfaces of the collection framework are in package java.util.

