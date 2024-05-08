class Queue:
    def __init__(self, capacity):
        self.capacity = capacity
        self.items = []

    def enqueue(self, item):
        if len(self.items) < self.capacity:
            self.items.append(item)
        else:
            print("Queue is full")

    def dequeue(self):
        if len(self.items) > 0:
            return self.items.pop(0)
        else:
            print("Queue is empty")

    def front(self):
        if len(self.items) > 0:
            return self.items[0]
        else:
            print("Queue is empty")

    def size(self):
        return len(self.items)

    def print_queue(self, message):
        print(message, self.items)

q = Queue(10)
q.enqueue("ra'na")
q.enqueue("vez")
q.enqueue("Arya")
q.print_queue("queue size is:")
print(q.dequeue(), "left the queue")
print("front of queue is:", q.front())
q.enqueue("milda")
q.dequeue()
q.dequeue()
q.dequeue()
print("It was a queue.")
print('queue size is:', q.size())
print('ra\'na', 'left the queue')
print('front of queue is:', q.front())
print('It was a queue.')