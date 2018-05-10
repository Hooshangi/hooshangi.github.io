


Go to SHOOSH room and participate in the quiz at: <a href="https://b.socrative.com/login/student/" target="_blank"> ![Socrative](images/logo_small_socrative.png)  
</a>

### Follow along and visualize your code  
*   <a href="http://pythontutor.com/live.html#mode=edit" target="_blank">Live programming</a>


### Useful links:
*   <a href="https://docs.python.org/3/faq/design.html#how-does-python-manage-memory" target="_blank">How does Python manage memory?</a>
*   <a href="https://docs.python.org/3/faq/design.html#how-are-lists-implemented" target="_blank"> How are lists implemented in Python?</a>
*   <a href="https://docs.python.org/3/c-api/memory.html" target="_blank"> In-depth overview of memory management in Python </a>
*   <a href="https://wiki.python.org/moin/TimeComplexity" target="_blank"> Time-complexity ("Big-Oh") in Python</a>


### In-class sample codes 

##### Create a node class, instantiate node objects, and then link the nodes
```python
#Node class declaration and instantiation
class Node:
    # The constructor 
    def __init__(self,data):
        self.data = data
        self.next = None

#Instantiate node objects
two=Node(2)
five=Node(5)
twenty=Node(20)

#Link the nodes
two.next=five
five.next=twenty
```

##### Create a linked list class 
Create a linked list class.
Include a method to add new node to the beginning of the linked list.
The head will always point to the most recently added node.

```python
# Create a linked list
class Node:
    def __init__(self,data):
        # The constructor
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        # The constructor
        self.head = None
        
    def add(self,data):
        # A method to add nodes to the beginning of the list
        new_node=Node(data)
        new_node.next=self.head
        self.head=new_node
    
mylist=LinkedList()
mylist.add(20)
mylist.add(5)
mylist.add(2)
```


##### Traverse and search
```python
class Node:
    def __init__(self,data):
        # The constructor
        self.data = data
        self.next = None 
  
class LinkedList:
    def __init__(self):
        # The constructor
        self.head = None

    def add(self,data):
        new_node=Node(data)
        new_node.next=self.head
        self.head=new_node
              
    def walk_through(self):
        #use an external reference to go through the nodes
        current = self.head
        while current != None :
            print(current.data)
            current = current.next

    def search(self,item):
        current = self.head
        found = False
        while current != None and not found:
            if current.data == item:
                found = True
            else:
                current = current.next
        return found              
            

if __name__=="__main__":
    mylist = LinkedList()
    mylist.add(20)
    mylist.add(10)
    mylist.add(5)
    
    mylist.walk_through()
    print(mylist.search(10))
    print(mylist.search('hello'))

```
 
##### Stack Implementation 
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class Stack:
    def __init__(self):
        self.head = None
        
    def is_empty(self):
        return self.head == None
   
    def push(self,data):
        new_node=Node(data)
        new_node.next=self.head
        self.head=new_node
     
    def pop(self):
        if (self.is_empty()):
            raise IndexError("empty list")      
        else:
            temp=self.head
            self.head=self.head.next
            popped=temp.data
            return popped
    
if __name__=="__main__":
    my_stack = Stack()
    my_stack.push(20)
    my_stack.push(10)
    my_stack.push(5)
    my_stack.push(1)
        
    print(my_stack.pop()) 
    
```

##### Queue Implementation 
```python

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class Queue:
    def __init__(self):
        self.head = None
        self.tail=None
        
    def is_empty(self):
        return self.head == None

    def enqueue(self,data):
        new_node=Node(data)

        if self.tail is not None:
            # make the front attribute of old node point to new node
            self.tail.next=new_node            
        else:
            # if first ever node in Queue both front and tail will point to it
            self.head = new_node

        self.tail = new_node


    def dequeue(self):
        if (self.is_empty()):
            raise IndexError("empty list")  
        temp=self.head
        self.head=self.head.next
        popped=temp.data
        return popped        


if __name__=="__main__":
    my_queue = Queue()
    my_queue.enqueue(20)
    my_queue.enqueue(10)
    my_queue.enqueue(5)
    my_queue.enqueue(1)
        
    my_queue.dequeue()  


```
 
