# Exp No: 36  
## Circular Queue 
---

### AIM  
To write a Python program with a function to insert float values into a Circular Queue.

---

### ALGORITHM

1. Start  
2. Check if the Circular Queue is full  
   - If `size == max_size`, print `"Queue is full"` and exit the function  
3. If the queue is not full:  
   - Read the element to be inserted  
   - Convert it to float  
   - Insert the element at the `tail` position  
   - Update tail using: `tail = (tail + 1) % max_size` (circular increment)  
   - Increment `size` by 1  
4. End


### PROGRAM

```
Reg.No: 212223060305
Name: Vishnu Priya E

class CircularQueue:
    def __init__(self, size):
        self.size = size
        self.queue = [0] * size
        self.front = -1
        self.rear = -1

    def enqueue(self, value):

        if (self.rear + 1) % self.size == self.front:
            print("Queue is full")
            return

        if self.front == -1:
            self.front = self.rear = 0
        else:
            self.rear = (self.rear + 1) % self.size

        self.queue[self.rear] = value

    def display_full_queue(self):
        return self.queue

cq_size = int(input())  
cq = CircularQueue(cq_size)

while True:
    try:
        num = input()
        if num == '':
            break
        cq.enqueue(int(num))
    except:
        break

print(cq.display_full_queue())


```

### OUTPUT
<img width="713" height="449" alt="image" src="https://github.com/user-attachments/assets/582066fa-4ab0-4a30-83ce-c77de751bf22" />

### RESULT
Thus the Python program with a function to insert float values into a Circular Queue is implemented and executed successfully.
