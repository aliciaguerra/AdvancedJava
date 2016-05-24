The ArrayList class extends AbstractList and implements the List interface. ArrayList supports dynamic arrays that
can grow as needed.

Standard Java arrays are of a fixed length. After arrays are created, they cannot grow or shrink, which means you must 
know in advance how many elements an array will hold.

Arraylists are created with an initital size. When the size is exceeded, the collection is automatically enlarged. 
When objects are removed, the array must be shrunk.

- ArrayList()
  This constructor builds an empty array list.
- ArrayList(Collection c)
  The constructor builds an array list that is initialized with the elements of the collection c
- ArrayList(int capacity)
  The constructor builds an array list that has the specified initial capacity. The capacity is the size of the underlying 
  array that is used to store the elements.  The capacity grows automatically as elements are added to an array list.
  
Apart from the methods inherited from the parent classes, ArrayList defines the following methods:

- void add(int index, Object element)
  Inserts the specified element at the specified position index in this list. Throws IndexOutOfBoundsException if the 
  specified index is out of range (index<0||index>size())
- boolean add(Object o)
  Appends the specified amount to the end of the list
- boolean addAll(Collection c)
  Appends all of the elements in the specified collection to the end of this list, in the order that they are returned by the specified collection's iterator. Throws NullPointerException if the specified collection is null.
