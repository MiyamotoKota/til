## 配列
### 行列入れ替え
import numpy as np  
arr=np.arange(9).reshape((3,3))  
arr.T もしくは、 arr.transpose((1,0))  

### 配列同士の内積の和
np.dot(arr.T, arr)  
