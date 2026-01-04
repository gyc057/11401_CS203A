# Array
## Definition
- 陣列是一個集合，裡面的每個位置都是連續的，每個元素都可透過索引(index)儲存以及查詢
## Array Type
### a. Static Array (靜態陣列)
#### Characteristic
##### Size
1. 陣列大小固定
2. 在宣告陣列時就要決定好大小
##### Element Type
1. 所有元素的型態一致
- Ex: int, string, char, bool and more...
##### Advantage in Efficiency
1. 因為陣列具有index，所以在存取以及查詢上非常迅速
2. 存取以及查詢的時間複雜度為 O(1)
##### Disadvantage in Efficiency
1. 由於位置固定，所以在插入和刪除的效率較差
2. 需要先搜索過整個陣列，找到要插入或刪除的位置或元素，所以時間複雜度為 O(n)
3. 因為在宣告時就已經決定了陣列的大小，所以當元素很少，空間大，就會造成空間的浪費，空間利用率下降
### b. Dynamic Array (動態陣列)
#### Size
1. 不須在一開始就宣告一個已經決定好大小的陣列
2. 視情況增加空間，ex: push_back()
#### Element Type
1. 與靜態陣列一樣，陣列中的所有元素的型態必須一致
-  Ex: int, string, char, bool and more...
#### Advantage in Efficiency
1. 因為陣列具有index，所以在存取以及查詢上非常迅速
2. 存取以及查詢的時間複雜度為 O(1)
3. 在有需要的情況下增加空間，所以不會造成空間上的浪費，空間利用率佳
#### Disadvantage in Efficiency
1. 由於位置固定，所以在插入和刪除的效率較差
2. 需要先搜索過整個陣列，找到要插入或刪除的位置或元素，所以時間複雜度為 O(n)