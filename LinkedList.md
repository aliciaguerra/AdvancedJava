The LinkedList class extends AbstractSequentialList and implements the data interface. It provides a linkedlist data 
structure.

- LinkedList()
  This constructor builds an empty linkedlist
- LinkedList (Collection c)
  The constructor builds a linked list that is initialized with the elements of the collection c.
  
Apart from the methods inherited from the parent classes, LinkedList define the following methods:

- void add(int index, Object element)
  Inserts the specified element at the specified position index in the list. Throws IndexOutOfBoundsException if the
  specified index is out of a range (index<0 || index>size()).
- boolean add(Object o)
  Appends the specified element to the end of the list.
- boolean addAll(Collection c)
  Appends all the elements in the specified collection to the end of the list, in the order that they were returned
  by the specified collection's iterator. Throws NullPointerException if the specified collection is null.
- boolean addAll(int index, Collection c)
  Inserts all of the elements in the specified collection into the list, starting at the specified position. 
  Throws NullPointerException if the specified collection is null.
- void addFirst(Object o)
  Inserts the given element at the begininng of the list.
- void addLast(Object o)
  Appends the given element to the end of the list.
- void clear()
  Removes all of the elements from this list.
- Object clone()
  Returns a shallow copy of this LinkedList
- boolean contains(Object o)
  Returns true if the list contains the specified element. More formally, returns true if and only if this list contains
  at least one element e such that (o==null ? e==null: o.equals(e))
  
