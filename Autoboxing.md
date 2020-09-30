## Autoboxing
* Added in Java 5.0
* Boxing converts Wrapper Class objects and primitive variables into each other
* Only works if Wrapper Class matches primitive data type

``public class AutoBoxingTest {
   public static void main(String args[]) {
      int num = 10; // int primitive
      Integer obj = Integer.valueOf(num); // creating a wrapper class object
      System.out.println(num + " " + obj);
   }
}``

This can go both ways

``public class UnboxingTest {
   public static void main(String args[]) {
      Integer obj = new Integer(10); // Creating Wrapper class object
      int num = obj.intValue(); // Converting the wrapper object to primitive datatype
      System.out.println(num + " " + obj);
   }
}``

But you don't have to do the conversion yourself

``List<Integer> li = new ArrayList<>();
for (int i = 1; i < 50; i += 2)
    li.add(i);``

is really

``List<Integer> li = new ArrayList<>();
for (int i = 1; i < 50; i += 2)
    li.add(Integer.valueOf(i));``



* Incrementing works with Wrapper Classes thanks to Autoboxing

``public class Example {
  private static Integer count = 0;
  public static void main(String[] args) {
    for(int i = 0; i < 1000; ++i) {
      count += 1;
    }
  }
}``

* Be careful to only use Wrapper Class when necessary (memory)   




[Next](parseBoolean.md)
