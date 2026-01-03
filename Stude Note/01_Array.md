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