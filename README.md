# linked-list-and-array-list
import java.util.ArrayList;
import java.util.LinkedList;
import java.util.List;
import java.util.Scanner;
public class SimpleUserInputListManipulation {
public static void main(String[] args) {
// Create a linked list and an array list
LinkedList&lt;Integer&gt; linkedList = new LinkedList&lt;&gt;();
ArrayList&lt;Integer&gt; arrayList = new ArrayList&lt;&gt;();
List&lt;Integer&gt; commonList;
// Get the list of integers from the user
Scanner scanner = new Scanner(System.in);
System.out.print(&quot;Enter integers separated by spaces: &quot;);
String input = scanner.nextLine();
// Parse the input string and add elements to both lists
String[] elements = input.split(&quot;\\s+&quot;);
for (String element : elements) {
int number = Integer.parseInt(element);
linkedList.add(number);
arrayList.add(number);
}
// Display initial lists
System.out.println(&quot;Initial Linked List: &quot; + linkedList);
System.out.println(&quot;Initial Array List: &quot; + arrayList);
// Get elements to be added from the user
System.out.print(&quot;Enter elements to be added (separated by spaces): &quot;);
String elementsToAddInput = scanner.nextLine();
String[] elementsToAdd = elementsToAddInput.split(&quot;\\s+&quot;);
// Add elements at the beginning and end of both lists
linkedList.addFirst(Integer.parseInt(elementsToAdd[0]));

arrayList.add(0, Integer.parseInt(elementsToAdd[0]));
linkedList.addLast(Integer.parseInt(elementsToAdd[1]));
arrayList.add(Integer.parseInt(elementsToAdd[1]));
// Display the final lists
System.out.println(&quot;Final Linked List: &quot; + linkedList);
System.out.println(&quot;Final Array List: &quot; + arrayList);
// Close the scanner to avoid resource leaks
scanner.close();
}
}

Output
Enter integers separated by spaces: 10 20 30 40
Initial Linked List: [10, 20, 30, 40]
Initial Array List: [10, 20, 30, 40]
Enter elements to be added (separated by spaces): 5 50
Final Linked List: [5, 10, 20, 30, 40, 50]
Final Array List: [5, 10, 20, 30, 40, 50]
