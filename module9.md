
EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:
```
#include <stdio.h>
#define MAX 100
int stack[MAX];
int top = -1;

void display() {
    if(top == -1) {
        printf("Stack is empty\n");
        return;
    }
    
    printf("Stack elements: ");
    for(int i = 0; i <= top; i++) {
        printf("%d ", stack[i]);
    }
    printf("\n");
}

int main() {
    int n, val;
    
    printf("Enter number of elements: ");
    scanf("%d", &n);
    
    for(int i = 0; i < n; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%d", &val);
        stack[++top] = val;
    }
    
    display();
    
    return 0;
}
```

Output:

<img width="620" height="302" alt="image" src="https://github.com/user-attachments/assets/26d639e5-2b85-421e-8a5e-4a78573a9b48" />


Result:

Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
```

#include <stdio.h>
float stack[SIZE];
int top = -1;

void push(float val) {
    if(top == SIZE - 1) {
        printf("Stack overflow\n");
        return;
    }
    
    stack[++top] = val;
    printf("%.2f pushed to stack\n", val);
}

int main() {
    int n;
    float val;
    
    printf("Enter number of elements: ");
    scanf("%d", &n);
    
    for(int i = 0; i < n; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%f", &val);
        push(val);
    }
    
    return 0;
}
```
Output:

<img width="616" height="367" alt="image" src="https://github.com/user-attachments/assets/0ddbee4c-4614-4d10-af1c-e501572d21be" />


Result:

Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:

To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:
```
#include <stdio.h>
int queue[MAX];
int rear = -1;
int front = -1;

void display() {
    if(front == -1) {
        printf("Queue is empty\n");
        return;
    }
    
    printf("Queue elements: ");
    for(int i = front; i <= rear; i++) {
        printf("%d ", queue[i]);
    }
    printf("\n");
}

int main() {
    int n, val;
    
    printf("Enter number of elements: ");
    scanf("%d", &n);
    
    for(int i = 0; i < n; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%d", &val);
        
        if(front == -1) {
            front = 0;
        }
        queue[++rear] = val;
    }
    
    display();
    
    return 0;
}
```

Output:

<img width="602" height="305" alt="image" src="https://github.com/user-attachments/assets/f01f4eb2-69b8-458d-9db3-65951645599a" />

Result:

Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```
#include <stdio.h>
float queue[SIZE];
int rear = -1;
int front = -1;

void enqueue(float val) {
    if(rear == SIZE - 1) {
        printf("Queue overflow\n");
        return;
    }
    
    if(front == -1) {
        front = 0;
    }
    
    queue[++rear] = val;
    printf("%.2f inserted to queue\n", val);
}

int main() {
    int n;
    float val;
    
    printf("Enter number of elements: ");
    scanf("%d", &n);
    
    for(int i = 0; i < n; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%f", &val);
        enqueue(val);
    }
    
    return 0;
}
```

Output:

<img width="512" height="350" alt="image" src="https://github.com/user-attachments/assets/2382579e-ab08-4971-ac12-6997981e0ccc" />


Result:

Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:

```
#include <stdio.h>
int queue[MAX];
int rear = -1;
int front = -1;
void dequeue() {
    if(front == -1) {
        printf("Queue is empty\n");
        return;
    }    
    printf("Deleted element: %d\n", queue[front]);
    front++;    
    if(front > rear) {
        front = rear = -1;
    }
}
int main() {
    int n, val;    
    printf("Enter number of elements: ");
    scanf("%d", &n);
        for(int i = 0; i < n; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%d", &val);
        if(front == -1) {
            front = 0;
        }
        queue[++rear] = val;
    }
    
    printf("Queue before deletion:\n");
    for(int i = front; i <= rear; i++) {
        printf("%d ", queue[i]);
    }
    printf("\n");
    
    dequeue();
    
    printf("Queue after deletion:\n");
    if(front != -1) {
        for(int i = front; i <= rear; i++) {
            printf("%d ", queue[i]);
        }
        printf("\n");
    } else {
        printf("Queue is empty\n");
    }
    
    return 0;
}
```
Output:

<img width="569" height="438" alt="image" src="https://github.com/user-attachments/assets/99ec6d72-458e-4851-9d4d-eaaa620c620d" />



Result:

Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
