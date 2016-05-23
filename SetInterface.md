A set is a collection that cannot contain duplicate elements. It models the mathematical set abstraction. 

The set interface contains only methods inherited from Collection and adds the restriction that duplicate elements are
prohibited.

Set also adds stronger contact on the behavior of the equals and hashCode operations, allowing set interfaces to be compared
meaningfully even if their implementation types differ.

- add()
  Adds an object to the collection
- clear()
  Removes all objects from the collection
- contains()
  Returns true if a specified object is an element within the Collection
- isEmpty()
  Returns true if the collection has no elements
- iterator()
  Returns an iterator for the collection which may be used to retrieve an object
- remove()
  Removes a specified object from within the collection
- size()
  Returns the number of elements in the collection
  
<h2>Example</h2>  
Set have its implmentation in various classes like HashSet, TreeSet, and LinkedHashSet. 

                          import java.util.*;
                          public class SetDemo {
                          public static void main(String args[]) {
                          int count[] = {34, 22, 10, 60, 30, 22};
                          Set<Integer> set = new HashSet<Integer>();
                          try {
                           for(int i=0; i<5; i++) {
                           set.add(count[i]);
                              }
                           System.out.println(set);
                           
                           TreeSet sortedSet = new TreeSet<Integer>(set);
                           System.out.println("The sorted list is: ");
                           System.out.println(sortedSet);
                           
                           System.out.println("The first element of the set is" + (Integer)sortedSet.first());
                           System.out.println("The last element of the set is:" + (Integer)sortedSet.last());
                           }
                           catch(Exception e){}
                              }
                          }

RESULT

                          [amrood]$ java SetDemo
                          [34, 30, 60, 10, 22]
                          The sorted list is:
                          [10, 22, 30, 34, 60]
                          The First element of the set is: 10
                          The last element of the set is: 60
