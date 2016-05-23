The Map.Entry interface enables you to move with a map entry. 

The entrySet() method declared by the Map interface returns a Set containing the map entries. Each of these Set elements
is a Map.Entry object.

METHODS

- boolean equals(Object obj)
  Returns true if obj is a Map.Entry whose key and value are equal to that of the invoking object.
- Object getKey()
  Returns the key for this map entry.
- Object getValue()
  Returns the value for this map value
- int hashCode()
  Returns the hash code for this map entry
- Object setValue(Object v)
  Sets the value for this map entry to v. A ClassCastException is thrown if v is not the correct type for the map. 
  A NullPointerException is thrown if v is null and the map does not permit null keys.
  
<h2>Example</h2>

                         import java.util.*;
                         public class HashMapDemo {
                          public static void main(String args[]) {
                           //Create a Hash Map
                           HashMap hm= new HashMap();
                           //Put elements to the map
                           hm.put("Zara", new Double(3434.3434));
                           hm.put("Mahnaz", new Double(123.22));
                           hm.put("Ayan", new Double(1378.00));
                           hm.put("Daisy", new Double(99.22));
                           hm.put("Qadir", new Double(-19.08));
                           
                           //Get a set of the entries
                           Set set = hm.entrySet();
                           //Get an iterator
                           Iterator i = set.iterator();
                           //Display elements
                           while(i.hasNext()) {
                            Map.Entry me = (Map.Entry)i.next();
                            System.out.println(me.getKey() + ":");
                            System.out.println(me.getValue());
                            }
                            System.out.println();
                            //Deposit 1000 into Zara's account
                            double balance = ((Double)hm.get("Zara")).doubleValue();
                            hm.put("Zara", new Double(balance+1000));
                            System.out.println("Zara's new balance" + hm.get("Zara"));
                               }
                            }
                            
RESULT

                            Daisy 99.22
                            Qadir: -19.08
                            Zara: 3434.34
                            Ayan: 1378.0
                            Mahnaz: 123.22
                            Zara's new balance: 4434.34
