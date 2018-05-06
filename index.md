
### POP QUIZ 
Participate in quizzes at: <a href="https://b.socrative.com/login/student/" target="_blank"> ![Socrative](images/logo_small_socrative.png)  
</a>

### Follow along and visualize your code  
*   <a href="http://pythontutor.com/live.html#mode=edit" target="_blank">Live programming</a>


### Useful links:
*   <a href="https://docs.python.org/3/faq/design.html#how-does-python-manage-memory" target="_blank">How does Python manage memory?</a>
*   <a href="https://docs.python.org/3/faq/design.html#how-are-lists-implemented" target="_blank"> How are lists implemented?</a>
*   <a href="https://docs.python.org/3/c-api/memory.html?highlight=memory" target="_blank"> Indept overview of memory </a>
*   <a href="https://wiki.python.org/moin/TimeComplexity" target="_blank"> Time-complexity ("Big O") in Python</a>


### Class Code 
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


### There's a horizontal rule below this.


