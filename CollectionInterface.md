The Collection interface is the foundation upon which the collections framework is built. It declares the core methods
that all collections will have. These methods are summarized in the following table.

Because all collections implement Collection, familiarity with its methods is necessary for a clear understanding of the
framework. Several of these methods can throw an UnsupportedOperationException.

- boolean add(Object obj)
  Adds obj to the invoking collection. Returns true if obj was added to the collection. Returns false if the obj is already
  a member of the collection, or if the collection does not allow duplicates. 
- boolean addAll(Collection c)
  Adds all the elements of c to the invoking collection. Returns true if the operation suceeded (i.e. the elements were added). Otherwise, returns false.
- void clear()
  Removes all elements from the invoking collection.
- boolean contains(Object obj)
  Returns true if the object is an element of the invoking collection. Otherwise, returns false.
- boolean containsAll(Collection c)
  Returns true if the invoking collection contains all elements of c. Otherwise, returns false.
- boolean equals(Object obj)
  Returns true if the invoking collection and object are equal. Otherwise, returns false.
- int hashCode()
  Returns the hash code for the invoking collection.
- boolean isEmpty()
  Returns true if the invoking collection is empty. Otherwise, returns false.
- Iterator iterator()
  Returns an iterator for the invoking collection.
- boolean remove(Object ob)
  Removes one instance of obj from the invoking collection. Returns true if the element was removed. Otherwise, returns
  false.
- boolean removeAll(Collection c)
  Removes all elements of c from the invoking collection. Returns true if the collection changed (i.e. elements were removed). Otherwise, returns false.
- boolean retainAll(Collection c)
  Removes all elements from the invoking collection except those in c. Returns true if the collection changed (i.e. elements were removed). Otherwise, returns false.
- int size() 
  Returns the number of elements held in the invoking collection. 
- Object[] toArray()
  Returns an array that contaisn all the elements stored in the invoking collection. The array elements are copies of the
  collection elements. 
- Object[] toArray(Object array[])
  Returns an array containing only those collection elements whose type matches that of array.
  
EXAMPLE

                import java.util.*;
                public class CollectionsDemo {
                 public static void main(String args[]) {
                 //ArrayList
                 List a1 = new ArrayList();
                 a1.add("Zara");
                 a1.add("Mahnaz");
                 a1.add("Ayan");
                 System.out.println("ArrayList elements");
                 Suystem.out.print("\t" + a1);
                 
                 //LinkedList
                 List L1 = new LinkedList();
                 l1.add("Zara");
                 l1.add("Mahnaz");
                 l1.add("Ayan");
                 System.out.println("LinkedList elements");
                 System.out.print("\t" + s1);
                 
                 //HashSet
                 Set s1 = new HashSet();
                 s1.add("Zara");
                 s1.add("Mahnaz");
                 s1.add("Ayan");
                 System.out.println("Set elements");
                 System.out.println("\t" + s1);
                 
                 //HashMap 
                 Map m1 = new HashMap();
                 m1.put("Zara", "8");
                 m1.put("Mahnaz", "31");
                 m1.put("Ayan", "12");
                 m1.put("Daisy", "14");
                 System.out.println();
                 System.out.println("Map Elements");
                 System.out.print("\t" + m1);
                      }
                }

RESULT

                           ArrayList Elements
                          [Zara, Mahnaz, Ayan]
                           LinkedList Elements
                          [Zara, Mahnaz, Ayan]
                           Set Elements
                          [Zara, Mahnaz, Ayan]
                          Map Elements
                          {Mahnaz=31, Ayan=12, Daisy=14, Zara=8}
