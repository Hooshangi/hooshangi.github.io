


Participate in quizzes at: <a href="https://b.socrative.com/login/student/" target="_blank"> ![Socrative](images/logo_small_socrative.png)  
</a>

### Follow along and visualize your code  
*   <a href="http://pythontutor.com/live.html#mode=edit" target="_blank">Live programming</a>


### Useful links:
*   <a href="https://docs.python.org/3/faq/design.html#how-does-python-manage-memory" target="_blank">How does Python manage memory?</a>
*   <a href="https://docs.python.org/3/faq/design.html#how-are-lists-implemented" target="_blank"> How are lists implemented?</a>
*   <a href="https://docs.python.org/3/c-api/memory.html?highlight=memory" target="_blank"> Indept overview of memory </a>
*   <a href="https://wiki.python.org/moin/TimeComplexity" target="_blank"> Time-complexity ("Big O") in Python</a>


### Class code 

##### Create a node class and link nodes
```python
#Node class declaration and instantiation
class Node:
    # The constructor 
    def __init__(self,data,next=None):
        self.data = data
        self.next = next

#Instantiate node objects
two=Node(2)
five=Node(5)
twenty=Node(20)

#Link the nodes
two.next=five
five.next=twenty
```

Create a linked list class 
Add new node to the beginning of the linked list
The head will always point to the most recently added node

```python
# Create a linked list

class Node:
    def __init__(self,data,next=None):
        self.data = data
        self.next = next

class LinkedList:
    def __init__(self):
        self.head = None
        
    def add(self,data):
        new_node=Node(data)
        new_node.next=self.head
        self.head=new_node
    
mylist=LinkedList()
mylist.add(20)
mylist.add(5)
mylist.add(2)
```

A more Pythonic approach

```python
class Node:
    def __init__(self,data,next=None):
        self.data = data
        self.next = next
    def set_next(self, newnext):
        self.next = newnext    

class LinkedList:
    def __init__(self):
        self.head = None
        self.length=0

    def add(self,data):
        new_node=Node(data)
        new_node.set_next(self.head)
        self.head=new_node
        self.length=self.length+1
 

if __name__=="__main__":
    mylist = LinkedList()
    mylist.add(20)
    mylist.add(10)
    mylist.add(5)
```

### There's a horizontal rule below this.


