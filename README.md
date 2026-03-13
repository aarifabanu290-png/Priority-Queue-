# Priority-Queue-
Data Structure Practicle program

16.Priority Queue using List

class PriorityQueue:
    def __init__(self):
        self.queue = []

    def insert(self, item):
        self.queue.append(item)

    def delete(self):
        if len(self.queue) == 0:
            return "Queue Empty"

        max = 0
        for i in range(len(self.queue)):
            if self.queue[i] > self.queue[max]:
                max = i

        item = self.queue[max]
        del self.queue[max]
        return item

pq = PriorityQueue()

pq.insert(10)
pq.insert(30)
pq.insert(20)

print("Deleted element:", pq.delete())
print("Deleted element:", pq.delete())

Output:
Deleted element: 30
Deleted element: 20
