<img alt="js" src="https://img.shields.io/badge/JavaScript-DataStructure-blue" />

## Linked Lists
> Linked lists are a foundational data structure used by many complex data structures.
> > <p>The key component of a linked list is a <strong>node</strong>. Other advanced data structures use nodes, too, but in a linked list specifically, a node is a unit containing two things at the same time:</p>
> > <ul>
> > <li>A <em>data</em> property that stores a value.</li>
> > <li>A <em>next</em> property, sometimes called a “pointer,” that points to the next item in the list.</li>
> > </ul>
```ruby
// each node contains two
class ListNode {
  constructor(data) {
    this.data = data; // data
    this.next = null; // pointer
  }
}

class LinkedList {
  constructor(head=null) {
    this.head = head;
  }

  size() {
    let count = 0;
    let node = this.head;
    while(node) {
      count ++;
      node = node.next
    }
    return count;
  }

  clear() {
    this.head = null;
  }

  getLast() {
    let getLast = this.head;
    while(getLast) {
      getLast = getLast.next;
    }
    return getLast;
  }

  getFirst() {
    return this.head;
  }
}

let node1 = new ListNode(2);
let node2 = new ListNode(5);

node1.next = node2;

let list = new LinkedList(node1);

console.log(list.head.next.data);
console.log(list.size())
```