# Stack and Queue
## Stack
### Definition
- Stack是一種資料結構，遵循後進先出(Last In First Out)的規則，也就是最後被放入的元素會最先被提出

Example

![alt text](LIFO-Operations-in-stack.jpg)
Resource: https://www.geeksforgeeks.org/dsa/lifo-principle-in-stack/
### Core Operation
1. Push: 從頂端加入元素
2. Pop: 從頂端移出元素
3. Top: 檢查頂端元素但不移除
4. Isempty: 檢查是否為空的堆疊(Stack)
## Queue
### Definition
- Queue是一種資料結構，遵循先進先出(First In First Out)的規則，也就是最先被放入的元素會最先被取出

Example

![alt text](First-In-First-Out-Queue-1024x683.png)
Resource: https://www.masaischool.com/blog/queue-data-structure-types-applications-javascript-implementation/
### Core Operation
1. Inqueue: 將元素加入末端(Rear)
2. Dequeue: 從前端(Front)移除元素
3. Front: 查看前端元素
4. Isempty: 檢查是否為空的佇列(Queue)
### Type of Queue
1. Circlar Queue(環狀佇列)
- 為了解決陣列實作佇列時，前端空間(Front)無法重複利用的問題，所以將頭尾串聯
2. Deque-Double-Ended Queue(雙向佇列)
- 允許前端與末段同時進行插入和刪除
3. Priority Queue(優先佇列)
- 每個元素都有權重或優先級，不會按照FIFO的規則操作
- 如果權重相同，則退回FIFO的規則進行操作