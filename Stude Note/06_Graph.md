# Graph
## Components of Graph & Each Component's Definition
- 節點(Vertex，符號V): 節點可以帶有數值。在同一張圖的所有節點可合為一個集合
- 邊(Edge，符號E): 連接兩節點的線，可帶有權重(Weight)、方向，在同一張圖的所有邊可合為一個集合
- 圖形(Graph，符號G): 圖形是由節點以及路徑組成 ---> G = (V, E)
- Example image:

![alt text](image-11.png)

## Types of Graph
1. Undirected Graph(無向圖)
- 沒有方向標示的邊
- Example image:

![alt text](image-12.png)

2. Directed Graph(有向圖)
- 有方向標示的邊
- Example image:

![alt text](image-13.png)

3. Weighted Graph(加權圖)
- 每個邊都有數值
- Example image:

![alt text](image-14.png)

4. Cyclic Graph(循環圖)
- 有封閉迴路的圖
- Example image:

![alt text](image-15.png)

5. Acyclic Graph
- 無封閉迴路的圖，也就是樹
- Example image:

![alt text](image-16.png)

6. Connected Graph
- 任意兩節點之間至少有一條邊，且無任何節點被孤立
- Example image:

![alt text](image-17.png)

## Graph Representation
- Adjacency Martrix
- Adjacency List
### Adjacency Martrix
- 用陣列的方式記錄每條邊
- Example image:

![alt text](image-18.png)

### Pros & Cons of Adjacency Matrix
- Pros
    1. 因為陣列具有index，所以在查詢兩節點之間使否相連的速度快
    2. 以二維陣列呈現，既清楚且較視覺化
    3. 適合儲存稠密圖，較不會浪費空間(因為節點和邊的數量多)
- Cons
    1. 如果要找出某節點的所有鄰居，需要查找遍整列才能完成，花費的時間較高$(O(V))$
    2. 在圖中的節點需要經常變動的情況下，整個陣列需要做插入或刪除的動作，非常耗時$(O(V^2))$
    3. 無法儲存重複的邊。標準的相鄰矩陣一個格子只能存一個值，難以表示兩點之間存在多條邊的情況
### Adjacency List
- 以Linked List的方式紀錄每條邊
- Example image:

<img width="680" height="235" alt="image" src="https://github.com/user-attachments/assets/92a1062a-2818-47f7-a245-f142a8a39fae" />

### Pros & Cons of Adjacency List
- Pros
    1. 因為空間可以動態調整，所以適合稀疏圖，空間複雜度為 $(O(V+E))$
    2. 查找某頂點的所有鄰居，只需要針對該點對應的串列進行搜查就好，不需像陣列一樣整列查一次，時間複雜度為 $(O(deg(V)))$
    3. 可以輕鬆處理大型且節點或邊容易變動的圖形
- Cons
    1. 在查詢兩節點是否有相連，要針對該點對應的串列搜查，時間複雜度為 $(O(deg(V)))$，相較於陣列的 $(O(1))$ 高
    2. 因為Linked List由指標連接，在實作上較二維陣列困難
    3. 若要刪除特定邊，需要搜索整個串列，時間複雜度為 $(O(deg(V)))$
## Breadth First Search (BFS)
- BFS為廣先搜尋，也就是先走訪完第一層的所有節點，再往第二層走訪
- 實作：利用Queue先進先出(FIFO)的特性，將要走訪的點一個一個放入陣列，再用一個陣列紀錄已走訪過的節點
- Example:

<img width="303" height="210" alt="image" src="https://github.com/user-attachments/assets/2347b5f4-2b3f-4cc5-ba0b-8d016fdc622e" />  

- Original: Queue: [], Visited Array: []  
- Step1: Queue[0], Visited Array: []
- Step2: Queue[1, 2, 3, 4], Visited Array: [0]
- Step3: Queue[2, 3, 4], Visited Array: [0, 1]
- Step4: Queue[3, 4, 6], Visited Array: [0, 1, 2]
- Step5: Queue[4, 6, 7], Visited Array: [0, 1, 2, 3]
- Step6: Queue[6, 7, 5], Visited Array: [0 ,1, 2, 3, 4]
- Step7: Queue[7, 5], Visited Array: [0, 1, 2, 3, 4, 6]
- Step8: Queue[5], Visited Array: [0, 1, 2, 3, 4, 6, 7]
- Step9: Queue[], Visited Array: [0, 1, 2, 3, 4, 6, 7, 5]
