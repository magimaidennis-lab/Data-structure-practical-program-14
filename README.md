# Data-structure-practical-program-14
class Node:
    def __init__(self,data):
        self.data=data
        self.next=None

class Stack:
    def __init__(self):
        self.top=None

    def push(self,data):
        new=Node(data)
        new.next=self.top
        self.top=new

    def pop(self):
        if self.top is None:
            return "No pages"
        temp=self.top
        self.top=self.top.next
        return temp.data

    def display(self):
        if self.top:
            print("Current Page:",self.top.data)

# Example
s=Stack()
s.push("Google")
s.push("YouTube")
s.push("Wikipedia")

s.display()
print("Back:",s.pop())
s.display()
Current Page: Wikipedia
Back: Wikipedia
Current Page: YouTube
