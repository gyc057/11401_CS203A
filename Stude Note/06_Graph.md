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