The SortedMap interface extends Map. It ensures that the entries are maintained in ascending key order.

Several methods throw a NoSuchElementException when no items are in the invoking map. A ClassCastException is thrown 
when an object is incompatible with the elements in the map. A NullPointerException is thrown if an attempt is made to use
a null object when null is not allowed in the map. 

- Comparator comparator()
  Returns the invoking sorted map's comparator. If the natural ordering is used for the invoking map, null is returned.
- Object firstKey()
  Returns the first key in the invoking map.
- SortedMap headMap(Object end)
  Returns a sorted map for those map entries with keys that are less than end.
- Object lastKey()
  Returns the last key in the invoking map.
- SortedMap subMap(Object start, Object end)
  Returns a map containing those entries with keys that are greater than or equal to start and less than end.
- SortedMap tailMap(Object start)  
  Returns a map containing those entries with keys that are greater than or equal to start.
  
EXAMPLE

                    import java.util.*;
                    public class TreeMapDemo {
                      public static void main(String args[]) {
                       TreeMap tm = new TreeMap();
                       //Put elements to the Map
                       tm.put("Zara", new Double(3434.34));
                       tm.put("Mahnaz", new Double(123.22));
                       tm.put("Ayan", new Double(1378.00));
                       tm.put("Daisy", new Double(99.22));
                       tm.put("Qadir", new Double(-19.08));
                       
                       //get a set of the entries
                       Set set = tm.entrySet();
                       //get an iterator
                       Iterator i = set.iterator();
                       //Display elements
                       while(i.hasNext()) {
                        Map.Entry me = (Map.Entry)i.next();
                        System.out.print(me.getKey() + ":");
                        System.out.println(me.getValue());
                        }
                        System.out.println();
                        //Deposit 1000 into Zara's account
                        double balance = ((Double)tm.get("Zara")).doubleValue();
                        tm.put("Zara", new Double(balance+1000));
                        System.out.println("Zara's new balance:" + tm.get("Zara");
                                    }
                        }
                        
RESULT

                       Ayan: 1378.0
                       Daisy 99.22
                       Mahnaz: 123.22
                       Qadir: -19.08
                       Zara: 3434.34
                       Zara.s current balance: 4434.34
