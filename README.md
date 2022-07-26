# -SM3_Birthday-Rho_attack
1.生日攻击。
这里我们选取足够多的随机字符串，将他们全部hash后的值进行对比，如果hash值重复，则说明攻击成功，我们将重复的hash值记录下来并输出，结果如下图所示。
![image](https://user-images.githubusercontent.com/106589212/181059088-c7aea3a9-1472-4eb8-aa48-d120936d3131.png)
2.将每次hash的结果都放入一个数组中，之后的每次hash都遍历数组，如果结果在数组中能够找到，说明攻击成功，如果没在数组中，则将此次hash结果放入数组并继续循环直到能在数组中找到结果。如图所示：
![image](https://user-images.githubusercontent.com/106589212/181059267-bde0de3a-85ac-4c0d-be3a-a34498166f78.png)
