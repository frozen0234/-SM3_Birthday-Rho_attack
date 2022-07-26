# -SM3_Birthday-Rho_attack

姓名：刘金星

学号：202000460060

git账户：frozen0234

1.生日攻击。

生日攻击建立在生日悖论上，我们对于n比特长的信息m，在2^n+1个数据中，至少能找到一对相等的数据；然而，要使我们从数据库中任意选出两个数据碰撞的概率接近100%，需要的数据量远比我们想象的要少。

通过对SM3的生日攻击，我们可以更好的确定SM3算法中哈希函数的输出长度。

在实现上，我们宏定义攻击长度n，我们任意选取两个信息m1和m2，不断尝试直到SM3(m1)与SM3(m2)的前n比特相等，即找到碰撞，输出相应的数据内容。通过改变长度n，对实验进行进一步研究。

这里我们选取足够多的随机字符串，将他们全部hash后的值进行对比，如果hash值重复，则说明攻击成功，我们将重复的hash值记录下来并输出，结果如下图所示。

![image](https://user-images.githubusercontent.com/106589212/181059088-c7aea3a9-1472-4eb8-aa48-d120936d3131.png)

2.Rho攻击。将每次hash的结果都放入一个数组中，之后的每次hash都遍历数组，如果结果在数组中能够找到，说明攻击成功，如果没在数组中，则将此次hash结果放入数组并继续循环直到能在数组中找到结果。如图所示：
![image](https://user-images.githubusercontent.com/106589212/181059267-bde0de3a-85ac-4c0d-be3a-a34498166f78.png)
