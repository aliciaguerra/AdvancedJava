The Enumeration Interface defines the methods by which you can enumerate (obtain one at a time) 
the elements in a collection of objects.

The legacy interface has been superceded by Iterator. Although not deprecated, Enumeration is considered obsolete
for new code. However, it is used by several methods defined by the legacy classes such as Vectors and Properties,
it is used by several other API classes, and is currently in widespread use in application code.

METHOD

- boolean hasMoreElements()
  When implemented, it must return true while there are still more elements to extract, and false when all the methods
  have been enumerated
- Object nextElement()
  This method returns the next object in the enumeration as a generic Object interface.
  
EXAMPLE

                 import java.util.Vector;
                 import java.util.Enumeration;
                 
                 public class EnumerationTester {
                 
                 public static void main(String args[]) {
                 Enumeration days;
                 Vector dayNames = new Vector();
                 dayNames.add("Sunday");
                 dayNames.add("Monday");
                 dayNames.add("Tuesday");
                 dayNames.add("Wednesday");
                 dayNames.add("Thursday");
                 dayNames.add("Friday");
                 dayNames.add("Saturday");
                 days = dayNames.elements();
                 while(days.hasMoreElements()) {
                  System.out.println(days.nextElement());
                              }
                          }
                      }    
                      
                 
