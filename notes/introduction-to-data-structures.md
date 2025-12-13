# Common Data Structures in JavaScript:

## Arrays:The All-Rounder
Arrays in JavaScript are like Swiss army knives - super versatile!

```javaScript
const fruits = ["apple", "banana", "blueberry"];
console.log(fruits[0]); // Outputs: apple
fruits.push("cherry");
console.log(fruits); // Outputs: ["apple", "banana", "blueberry", "cherry"]
```
---

## Objects: The Organizers
Objects help you store data in a key-value pair, making it easy to find what you need.

```javaScript
const car = {
    make: "Toyota",
    model: "Supra",
    year: 1993
};
console.log(car.model); // Outputs: Supra
```
---

## Stacks: The Last-In-First-Out (LIFO)
Stacks are like a stack of plates; the last one you put on top is the first one you take off.

```javaScript
class Stack {
    constructor() {
        this.items = [];
    };

    push(element) {
        this.items.push(element);
    };

    pop() {
        if (this.items.length === 0) return "Underflow"
        return this.items.pop()
    };

    peek() {
        return this.items[this.items.length - 1]
    };
};

let stack = new Stack();
stack.push(10);
stack.push(20);
console.log(stack.pop());
console.log(stack.peek());
console.log(stack.pop());
```
---

## Queues: The First-In-First-Out (FIFO)
Queues are like a line at a store; the first person in line is the first to get served.

```javaScript
class Queue {
    constructor() {
        this.items = [];
    };

    enqueue(element) {
        this.items.push(element);
    };

    dequeue() {
        if (this.items.length == 0) return "Underflow";
        return this.items.shift();
    };

    front() {
        if (this.items.length === 0) return "No elements in Queue";
        return this.items[0];
    };
}

let queue = new Queue();
queue.enqueue(10);
queue.enqueue(20);
console.log(queue.front()); // Outputs: 10
console.log(queue.dequeue()); // Outputs: 10
console.log(queue.front()); // Outputs: 20
```
---

## Linked Lists: The Flexible Connectors
Linked Lists consist of nodes where each node contains a value and a pointer to the next node in the list.

```javaScript
class Node {
    constructor(element) {
        this.element = element;
        this.next = null;
    }
}

class LinkedList {
    constructor() {
        this.head = null;
        this.size = 0;
    }

    add(element) {
        let node = new Node(element);
        let current;

        if (this.head == null) this.head = node; // If list is empty, make the new node the head
        else {
            current = this.head;
            while (current.next) {
                current = current.next; // Move to the next node until the end
            }
            current.next = node; // Add the new node to the end of the list
        }
        this.size++;
    }
}

let ll = new LinkedList();
ll.add(10);
ll.add(20);
console.log(ll); // Outputs the LinkedList with 10 and 20 as elements
```
---

## Trees: The Hierarchical Organizers
Trees are non-linear data structures used for storing hierarchical data like folders in a computer.

```javaScript
class TreeNode {
    constructor(data) {
        this.data = data
        this.children = []
    }

    addChild(child) {
        this.children.push(new TreeNode(child));
    }
}

let root = new TreeNode('root');
root.addChild('child1');
root.addChild('child2');
console.log(root); // Outputs the tree structure with root, child1, and child2
```