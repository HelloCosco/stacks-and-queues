# stacks-and-queues

//Beta
//Need help trying to figure out what to do next

public class StackOfInts {

   private static class Node {
      int item;
      Node next;
   }
   
   private Node top; 
   
   public void push( int N ) {
      Node newTop;         // A Node to hold the new item.
      newTop = new Node();
      newTop.item = N;     // Store N in the new Node.
      newTop.next = top;   // The new Node points to the old top.
      top = newTop;        // The new item is now on top.
   }
   public int pop() {
      if ( top == null )
         throw new IllegalStateException("Can't pop from an empty stack.");
      int topItem = top.item;  
      top = top.next;          
      return topItem;
   }
   
   public boolean isEmpty() {
      return (top == null);
   }

} 
