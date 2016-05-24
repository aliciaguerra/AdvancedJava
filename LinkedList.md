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
- Object get(int index)
  Returns the element at the specified position in the list. Throws IndexOutOfBoundsException if the specified index
  is out of range (index<0 || index>=size())
- Object getFirst()
  Returns the first element in the list. Throws NoSuchElementException if the list is empty.
- Object getLast()
  Returns the last element in the list. Throws NoSuchElementException if the last element is empty.
- int indexOf(Object o)
  Returns the index in this list of the first occurence of the specified element, or -1 if the List does not contain the 
  element.
- int lastIndexOf(Object o)
  Returns the index in this list of the last occurrence of the specified element, or -1 if the lsit does not contain
  this element.
- ListIterator listIterator(int index)
  Returns a ListIterator of the elements in this list (in proper sequence), starting at the specified position in the list.
  Throws IndexOutOfBoundException if the specified index is out of range (index<0 || index>=size())
- Object remove(int index)
  Removes the element at the specified position in the list. Throws NoSuchElementException if this list is empty.
- boolean remove(Object o)
  Removes the first occurrence of the specified element in the index. Throws NoSuchElementException if this list is
  empty. Throws IndexOutOfBoundsException if the specified index is out of range (index<0 || index>=size()).
- Object removeFirst()
  Removes and returns the first element in the list. Throw NoSuchElementException if this list is empty.
- Object removeLast()
  Removes and returns the last element from this last. Throws NoSuchElementException if this list is empty.
- Object set(int index, Object element)
  Replaces the element at the specified position in the list within the specified element. Throws IndexOutOfBoundsException
  if the specified index is out of range (index<0 || index>=size())
- int size()
  Returns the number of elements in this list.
- Object[] toArray()
  Returns an array containing all of the elements in this list in the correct order. Throws NullPointerException if the specified array is null.
- Object[] toArray(Object[] a)
  Returns an array containing all of the elements in this list in the correct order; the runtime type of the returned array
  is that of the specified array.

<h2>Example</h2>

                            import java.util.*;
                            public class LinkedListDemo {
                             public static void main(String args[]) {
                             //create a linked list
                             LinkedList ll = new LinkedList();
                             //add elements to the linked list
                             ll.add("F");
                             ll.add("B");
                             ll.add("D");
                             ll.add("E");
                             ll.add("C");
                             ll.addLast("Z");
                             ll.addFirst("A");
                             ll.add(1, "A2");
                             System.out.println("Original contents of ll:" + ll);
                             
                             //remove elements from the linked list
                             ll.remove("F");
                             ll.remove(2);
                             System.out.println("Contents of ll after deletion:" + ll);
                             
                             //get and set a value
                             Object val = ll.get(2);
                             ll.set(2, (String) val + "Changed");
                             System.out.println("ll after change:" + ll);
                                 }
                             }
                             
RESULT

                               Original contents of ll: [A, A2, F, B, D, E, C, Z]
                               Contents of ll after deletion: [A, A2, D, E, C, Z]
                               ll after deleting first and last: [A2, D, E, C]
                               ll after change: [A2, D, E Changed, C]
  
