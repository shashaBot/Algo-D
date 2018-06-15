# Enumeration

```
For example, let T(n) be count for n nodes.
T(0) = 1  [There is only 1 empty tree]
T(1) = 1
T(2) = 2

T(3) =  T(0)*T(2) + T(1)*T(1) + T(2)*T(0) = 1*2 + 1*1 + 2*1 = 5

T(4) =  T(0)*T(3) + T(1)*T(2) + T(2)*T(1) + T(3)*T(0)
     =  1*5 + 1*2 + 2*1 + 5*1 
     =  14 
```


The above pattern basically represents n’th Catalan Numbers. First few catalan numbers are 1 1 2 5 14 42 132 429 1430 4862,…
```T(n)=\sum_{i=1}^{n}T(i-1)T(n-i)=\sum_{i=0}^{n-1}T(i)T(n-i-1)=C_n```

Here,

T(i-1) represents number of nodes on the left-sub-tree

T(n−i-1) represents number of nodes on the right-sub-tree

n’th Catalan Number can also be evaluated using direct formula.

```
   T(n) = (2n)! / (n+1)!n!
```

Number of Binary Search Trees (BST) with n nodes is also same as number of unlabeled trees. The reason for this is simple, in BST also we can make any key as root, If root is i’th key in sorted order, then i-1 keys can go on one side and (n-i) keys can go on other side.

How many labeled Binary Trees can be there with n nodes?

To count labeled trees, we can use above count for unlabeled trees. The idea is simple, every unlabeled tree with n nodes can create n! different labeled trees by assigning different permutations of labels to all nodes.

Therefore,

```
Number of Labeled Tees = (Number of unlabeled trees) * n!
                       = [(2n)! / (n+1)!n!]  × n!
```
                       
For example for n = 3, there are 5 * 3! = 5*6 = 30 different labeled trees