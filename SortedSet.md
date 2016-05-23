The SortedSort interface extends Set and declares the behavior of a sorted set in ascneding order. In addition to those
methods defined by Set, the SortedSet interface declares the methods summarized in the table before:

Several methods throw a NoSuchElementException when no items are contained in the invoking set. A ClassCastException 
is thrown when an object is incompatible with the elements in a set. 

A NullPointerException is thrown if an attempt is made to use a null object  and null is not allowed in the set.

- Comparator comparator()
  Returns the invoking sorted set's comparator. If the natural ordering is used for this set, null is returned.
- Object first()
  Returns the first element in the invoking sorted set.
- SortedSet headSet(Object end)
  Returned a SortedSet containing those elements less than end that are contained in the invoking sorted set. Elements in
  the returned sorted set are also referenced by the invoking sorted set.
- Object last()
  Returns the last element in the invoked sorting set.
- SortedSet subSet(Object start, Object end)
  Returns a SortedSet that includes those elements between start and end. Elements in the returned collection are also
  referenced by the invoking object.
- SortedSet tailSet(Object start)
  Returns a SortedSet that contains those elements greater than or equal to start that are contained in the sorted set.
  Elements in the returned set are also referenced by the invoking set.
  
<h2>EXAMPLE</h2>  

                           import java.util.*;
                           public class SortedSetTest {
                            public static void main(Strin args[]) {
                            
                            //Create the sorted set
                            SortedSet set = new TreeSet();
                            
                            //Add elements to the set
                            set.add("b");
                            set.add("c");
                            set.add("a");
                            
                            //Iterating over the elements in the set
                            Iterator it = set.iterator();
                            while(it.hasNext()) {
                            //Get element
                            Object element = it.next();
                            System.out.println(element.toString());
                                         }
                                    }
                            }
                            
RESULT

                           a
                           b
                           c
