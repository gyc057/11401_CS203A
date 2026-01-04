# Linked List
## Definition
- 由節點(Nodes)連結而成，這些節點在記憶體中不必連續存放
## The Structure of Node
- Data: 儲存的數值
- Pointer: 用來指向下個節點的指標
## Type of Linked List
### a. Singly Linked List (單向鏈結)
1. 先有一個Head指標指向第一個節點，接著每個節點只指向下一個節點，最後一個節點指向NULL
![alt text](image.png)
### b. Doubly Linked List (雙向鏈結)
1. 頭尾分別有Head指標和Tail指標，Head指向第一個節點，Tail指向最後一個節點
2. 每個節點有兩個指標，分別指向前一個(Prev)與後一個(Next)的節點，方便雙向走訪

![alt text](image-1.png)
### c. Circular Linked List (環狀鏈結)
1. 連結方式與Singly Linked List大致相同，唯一差異在於將最後一個節點指向第一個節點，形成一個圓環。
![alt text](image-2.png)