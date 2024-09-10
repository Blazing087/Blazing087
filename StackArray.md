public class StackCustom {
	int top;
	int stackArray[];
	int maxsize;
	
	// Declaring the Variables
	public StackCustom(int size) {
		maxsize = size;
		stackArray = new int[maxsize];
		top =-1;
	}
	
	// Checking if the Stack is Empty.
	public boolean isEmpty() {
		return top == -1;
	}
	
	// Checking if the Stack is Full.
	public boolean isFull() {
		return top == maxsize - 1;
	}
	
	// Adding an Element in the Stack.
	public void push(int element) {
		if (isFull()) {
			System.out.println("Stack is Full!");
		}else {
			stackArray[++top] = element;
			System.out.print("Push Element:"+element+" ");
		}
	}
	
	// Removing the Top Element in the stack.
	public int pop() {
		if (isEmpty()) {
			System.out.println("Stack is Empty");
			return -1;
		}else {
			return stackArray[top--];
		}
	}
	
	// Outputting the Top Element.
	public int peek() {
		if (isEmpty()) {
			System.out.println("Stack is Empty!");
			return -1;
		}else {
			return stackArray[top];
		}
	}
	
	public static void main(String[] args) {
		StackCustom stack = new StackCustom(4);
		
		if(stack.isEmpty()) {
			System.out.println("Stack is Empty!");
		}
		System.out.println("======================================");
		
		stack.push(10);
		stack.push(30);
		stack.push(50);
		stack.push(40);
		
		System.out.println("\n======================================");
		
		System.out.println("Emement Popped:"+stack.pop());
		System.out.println("Emement Popped:"+stack.pop());
		System.out.println("Emement Popped:"+stack.pop());
		System.out.println("======================================");
		
	}
}
