The Map interface maps unique keys to values. A key is an object that you use to retrieve a value at a later date.

- Given a key and a value, you can store the value in a Map object. After the value is stored, you can retrieve it by 
  using its key.
- Several methods throw a NoSuchElementException when no items exist in the invoking map.
- A ClassCastException is thrown when an object is incompatible with the elements in a map.
- A NullPointerException is thrown if an attempt is made to use a null object and null is not allowed in the map.
- An UnsupportedOperationException is thrown when an attempt is made to change an unmodifiable map.

METHODS

- void clear()
  Removes all key/value pairs from the invoking map.
- boolean containsKey(Object k)
  Returns true if the invoking map contains v as a value. Otherwise, returns false.
- boolean containsValue(Object v)
  Returns true if the map contains v as the value. Otherwise, returns false.
- Set entrySet()
  Returns a set that contains the entries in the map. The set contains objects of the type Map.Entry. This method
  provides a set-view of the invoking map.
- boolean equals(Object obj)
  Returns true if obj is a Map and contains the same entries. Otherwise, returns false.
- Object get(Object k)
  Returns the value associated with the key K
- int hashCode()
  Returns the hash code for the invoking map.
- boolean isEmpty()
  Returns true if the invoking map is empty. Otherwise, returns false.
- Set keySet()
  Returns a Set that contains the keys in the invoking map.
- Object put(Object k, Object v)
  Puts an entry in the invoking map, overwriting any previous value associated with the key. The key and values are k
  and v respectively. Returns null if the key did not already exist. Otherwise, the previous value linked to the key
  is returned. 
- void putAll(Map m)
  Puts all the entries from m into this map
- Object remove(Object k)
  Removes the entry whos key equals zero
- int size()
  Returns the number of key/value pairs in the map
- Collection values()
  Returns the number of collection containing the values in the map. This method provides a collection-view of the values
  in the map.
  
<h2>Example</h2>
Map has its implementation in various classes like HashMap. Following is the example to explain Map functionality.

                     import java.util.*;
                     public class CollectionsDemo {
                       public static void main(String args[]) {
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
 
                      ap Elements
                      {Mahnaz=31, Ayan=12, Daisy=14, Zara=8}
                      
