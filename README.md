# 我的工具箱
## 安装

pip3 install -U git+https://source.enncloud.cn/heweichenga/My_Package.git
## 1、文件处理
#### 读取pickle文件
```python
from magic.file import FileHelper
with FileHelper(path="DIR",file_type="pickle") as fr:
        data=fr.load()
```
#### 写入pickle文件
```python
from magic.file import FileHelper
DATA=1
with FileHelper(path="DIR",file_type="pickle") as fr:
        data=fr.write(DATA)
```

#### 读取文本文件
```python
from magic.file import FileHelper
with FileHelper(path="DIR",file_type="txt") as fr:
        data=fr.load()
```

#### 程序时间计算
```python
from magic.tools import timer

@timer()
def func():
    n=0
    for i in range(100000):
        n+=1
    print(n)
```