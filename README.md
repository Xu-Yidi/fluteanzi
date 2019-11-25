# **Data Structure and Algorithm in Python**
此處文件包含自行整理之資料結構的handout與Leetcode的程式，handout包含資料結構的基本特性的描述（以註解方式給出）以及基本操作的Python程式<br>
[Git語言入門](https://zhuanlan.zhihu.com/p/30044692)
## Content
 [Week2(singly linked list)](#week2)<br>
 [Week3(stack & queue)](#week3)<br>
 [Week4(insertion sort & bubble sort & selection sort & time complexities)](#week4)<br>
 [Week5(quick sort)](#week5)<br>
 [Week6(heap data structure & heap sort)](#week6)<br>
 [Week7(merge sort)](#week7)<br>
 [Week8(binary tree)](#week8)<br>
 [Week9(binary search tree)](#week9)<br>
 [Week10(red-black trees)](#week10)<br>
 
## Week2
### Singly Linked List
[code-linked list的基本操作](/week2/handout-singly%20linked%20list.py)<br>
- **Linked List**<br>
1.A linked structure contains a collection of objects called nodes, each of which contains data and at least one reference or link to another node<br>
2.A linked list is a structure in which the nodes are connected in sequence to form a linear list<br>
>>(1)The first node in the list(***head node***), must be named or referenced by external variable<br>
>>(2)The last node in the list(***tail node***), is indicated by a null link reference<br>
>>(3)A linked list can be empty, which can be indicated when the head reference is null<br>
- **The Singly Linked List**<br>
1.a singly linked list is a linked list in which each node contains a single link field and allows for a complete traversal from a distinctive first node to the last<br>
- **LeetCode**<br>
[#707 design linked list](/week2/%23707%20design%20linked%20list.py)<br>
[#206 reverse linked list](/week2/%23206%20reverse%20linked%20list.py)<br>

[back to content](#content)<br>

## Week3
### Stack
[code-stack的array與linked list實現](/week3/handout-stack.py)<br>
- **The Stack ADT**<br>
1.inserted and removed sccording to the ***last-in, first-out(LIFO) principle***<br>
2.***top*** of the stack/ ***base*** of the stack<br>
3.basic operations:<br>
>>(1)**`isEmpty()`**: returna boolean value indicating if the stack is empty<br>
>>(2)**`getSize()`**: returns the number of items in the stack<br>
>>(3)**`pop()`**: remove and returns the top item of the stack, if the stack is not empty, and the next item on the stack becomes the new top item<br>
>>(4)**`push(item)`**: adds the given item to the top of the stack<br>
>>(5)**`peek()`**: returns a reference to the item on top of a non-empty stack without removing it<br>
- **Implementing the Stack**<br> 
1.the stack ADT can be implemented by the use of Python list and a linked list<br>
- **LeetCode**<br>
[#155 min stack](/week3/%23155%20min%20stack.py)<br>

### Queue
[code-circular queue的array與linked list實現&priority queue的array實現](/week3/handout-queue.py)<br>
- **The Queue ADT**<br>
1.items can only be added to one end and removed from the other, known as the ***first-in, first-out(FIFO)principle***<br>
2.new items are inserted into a queue at the ***rear*** while existing items are removed from the ***front***<br>
3.basic operations:<br>
>>(1)**`isEmpty()`**: return a boolean value indicating whether the queue is empty<br>
>>(2)**`getSize()`**: returns the number of items currently in the queue<br>
>>(3)**`enqueue(item)`**: adds the given item to the back of the queue<br>
>>(4)**`dequeue()`**: removes and returns the front item from the queue, an item can not be dequeued from an empty queue<br>
>>(5)**`getFront()`**: return a reference to the element at the front of queue without removing it, and an error occurs if the queue is empty<br>
>>(6)**`getRear()`**: return a reference to the element at the back of queue without removing it<br>
- **Implementing the Queue**<br>
1.implementation of the Queue ADT using a Python list<br>
2.**using a circular array**<br>
(1)a circular array is simply an array viewed as a circle instead of a line<br>
(2)allows to add new items to a queue and remove existing ones without having to shift items in the process<br>
(3)introduces the concept of a ***maximum-capacity queue*** that can become full<br>
(4)uesd with application that require small-capacity and allows for the specification of a maximum size<br>
(5)must maintain a count field and two markers:<br>
>>a.***count field***: to keep track of how many items are currently in the queue<br>
>>b.***front and rear***: to indicate the array elements containing the first and last items in the queue<br>
- **The Priority Queue**<br>
1.a priority queue is a queue with each item is assigned a priority and items with a high priority are removed before those with lower priority<br>
(1)***the bounded priority queue*** assumes a small limited range of p priorities over the interval of integers[0,p)<br>
(2)***the unbounded priority queue*** places no limit on the range of integer values that can be used as priorities<br>
(3)integer values are used for the priorities with a smaller integer value having a higher pripority<br>
2.basic operations:<br>
>>(1)**`PriorityQueue()`**: creates a new empty unbounded priority queue<br>
>>(or 1)**`BPriorityQueue(numLevels)`**: creates a new empty bounded priority queue with priority levels in the range from 0 to numLevels-1<br>
>>(2)**`isEmpty()`**<br>
>>(3)**`getSize()`**<br>
>>(4)**`enqueue(item, priority)`**: adds the given item to the queue by inserting it in the proper position based on the given pripority<br>
>>(5)**`deququq()`**: removes and returns the front item from the queue, which is the item with the highest priority,if two items have the same priority, then items are removed with FIFO order<br>
- **LeetCode**<br>
[#232 implement queue using stacks](/week3/%23232%20implement%20queue%20using%20stacks.py)<br>
[#622 design circular queue](/week3/%23622%20design%20circular%20queue.py)<br>

[back to content](#content)<br>

## Week4
[code-insertion sort & bubble sort & selection sort的實現](/week4/handout-sorting.py)
### Insertion Sort
- **Logic**<br>
1.partition the array into two regions: sorted and unsorted<br>
2.take each item from the unsorted region and insert it into its correct order in the sorted region<br>
- **Advantages and Disadvantages**<br>
1.adaptive, i.e. efficient for nearly-sorted datasets:smiley:<br>
2.in-place, i.e. requires a constant O(1) of additional memory space:smiley:<br>
3.slow for unsorted or reverse-sorted data:cry:<br>
4.needs a large number of element shifts:cry:<br>
- **Leetcode**<br>
[#147 insertion sort list](/week4/%23147%20insertion%20sort%20list.py)<br>

### Bubble Sort
- **Logic**<br>
1.go through multiple passes over the array<br>
2.in every pass:<br>
>>(1)compare adjacent elements in the list<br>
>>(2)exchange the elements if they are out of order<br>
>>(3)each pass moves the largest(or smallest) elements to the end of the array<br> 
3.repeating this process in several passes eventually sorts the array into ascending(or descending) order<br>

### Selection Sort
- **Logic**<br>
1.choose the largest/smallest item in the array and place the item in its correct place<br>
2.choose the next largest/next smallest item in the array and place the item in its correct place<br>
3.repeat the process until all items are sorted<br>

### Time Complexity
- **Asymptotic Notation(漸進符號)**<br>
<img height="75%" width="75%" src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week4/time_complexity1.JPG"><br>

- **The Most Common Time Complexities**<br>
<img height="75%" width="75%" src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week4/time_complexity2.jpeg"><br>

| Name | Time Complexity | Class|
| :-: | :-: | :-:|
| Constant time | O(1) | Polynomial time |
| Logarithmic time | O(logn) | Polynomial time |
| Linear time | O(n) | Polynomial time |
| Quasilinear time| O(nlogn)| Polynomial time |
| Quadratic time| O(n^2) | Polynomial time |
| Exponential time| O(2^n) | Non-deterministic polynomial time |
| Factorial time| O(n!) | Non-deterministic polynomial time |

- **How to Calculate Time Complexity**<br>

| Algorithm | Best Case | Average Case| Worst Case |
| :-: | :-: | :-:| :-: |
| Bubble Sort | O(n^2)/O(n) | O(n^2) | O(n^2) |
| Selection Sort | O(n^2) | O(n^2) | O(n^2) |
| Insertion Sort | O(n) | O(n^2) | O(n^2) |
| Quick Sort| O(nlogn)| O(nlogn) | O(n^2) |

<img height="75%" width="75%" src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week4/time_complexity3.JPG"><br>
<img height="75%" width="75%" src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week4/time_complexity4.JPG"><br>
 
 1.Big-O-Notation Rules<br>
 >>(1)**`Transitivity rule`**<br>
 >>If *f*(n) ∈ O(*g*(n)) and *g*(n) ∈ O(*h*(n)), then *f*(n) ∈ O(*h*(n))<br>
 >>(2)**`Addition rule`**<br>
 >>If *f*(n) ∈ O(*g*(n)) and *g*(n) ∈ O(*h*(n)), then *f*(n) + *g*(n) ∈ O(max(*g*(n),*h*(n)))<br>
 >>(3)**`Multiplication Rule`**<br>
 >>If *f*(n) ∈ O(*g*(n)) and *g*(n) ∈ O(*h*(n)), then *f*(n) * *g*(n) ∈ O(*g*(n) * *h*(n))<br>
[proof](https://www.cs.hmc.edu/~keller/cs60book/11%20Complexity.pdf)<br>

- **reference**<br>
[Complexity: Asymptotic Notation(漸進符號)](http://alrightchiu.github.io/SecondRound/complexityasymptotic-notationjian-jin-fu-hao.html)<br>
[知乎-如何清晰的理解算法中的时间复杂度？](https://www.zhihu.com/question/20196775)<br>
[CSDN-算法的时间复杂度和空间复杂度-总结](https://blog.csdn.net/zolalad/article/details/11848739)<br>

[back to content](#content)<br> 

## Week5
[code-quick sort使用額外空間與原地置換的實現](/week5/handout-quick_sort.py)
### Quick Sort
The quick-sort algorithm sorts a sequence S using a simple **recursiv** approach. The main idea is to apply the **divide-and-conquer** technique, whereby we divide S into subsequences, recur to sort each subsequence, and then combine the sorted subsequences by a simple concatenation<br>
- **Logic**<br>
1.**Divide**: If Seqence S has at least two elements, select a specific element x from s, called the pivot(usually the last element in S). Partition the sequence S into three subsequences:<br>
(1)***Less(Left)***: store the elements in S less than pivot x<br>
(2)***Equal***: store the elements in S equal to pivot x<br>
(3)***Greater(Right)***: store the elements in S greater than pivot x<br>
2.**Conquer**: Recurxively sort subsequences Less and Greater.<br>
3.**Combine**: Combine the sorted subsequenes by a simple concatenation<br>
- **Time Complexities**<br>
<img height="75%" width="75%" src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week5/quick_sort.JPG"><br>
<img height="75%" width="75%" src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week5/quick_sort2.JPG"><br>
[back to content](#content)<br> 

## Week6
### The Heap Data Struture
- The (Binary) heap *T* is an **array** object that can be viewed as a nearly **complete binary tree(完全二元樹)** and satisfies two additional properties: a relation property defined in terms of the ways are stored in *T* and a structural property defined in terms of the shape of *T* itself.<br>
>(1)**Heap-Order Property(relational property)**: In a heap *T*, for every position *p* other than the root, the key sorted at *p* is geater than or equal to the key stored at *p*'s parent.<br>
>(2)**Complete Binary Tree Property(strutural property)**: A heap *T* with height *h* is a complete binary tree if levels 0,1,...,*h*-1 of *T* have the maximum numbers of nodes possible(i.e. level *i* has 2^*i* nodes, for 0 ≤ *i* ≤ *h*-1) and the remaining nodes at level *h* reside in the leftmost possible at that level.<br>

- The **height** of a node in a heap is the number of edges on the longest simple downward path from the node to a leaf, and the height of the heap to be the height of the root.<br>
>(1)A heap *T* storing n entries has height ***h* = floor(log_2(*n*))**<br>
>(2)For example:<br>
the height of the heap is 3(a heap with height *h* has *h+1* levels)<br>
the height of the node 1 is 2<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week6/heap.jpg">

- If a complete binary tree with n nodes is represented sequentially, then for any node with index *i*, 0 ≤ *i* ≤ *n*-1, we have:
>(1)A[0] is the root of the tree<br>
>(2)the parent of node i: **parent(i) = floor((i-1)/2)**<br>
>(3)the left child of node i: **left(i) = 2i + 1**<br>
>(4)the right child of node i: **right(i) = 2i + 2**<br>

- Heap properties:<br>
>(1)**Max-heap**:the largest element in a max-heap is at the root and the subtree rooted at a node contains values no larger than that contained at the node itself, i.e. A[parent(i)] >= A[i].<br>
>(2)**Min-heap**:the smallest element in a min-heap is at the root and subtree rooted at a node contains values no smaller than that contained at the node itself, i.e. A[parent(i)] <= A[i]<br>

### Basic Procedures
- **shift-up**(insertion): To restore the heap order property, the new value has to move up along the path in reverse order from the root to the insertion point until a node is found where it can be positioned properly.<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week6/shift-up.jpg">

- **shift-down**(remove): After the value in the root has been removed, the value from the rightmost node on the lowest level is copied to the root and that leaf is removed. Then starting at the root node, the node's value is compared to its children and swapped with the larger of the two, and this process continues until the smaller value is copied into a leaf node or a node whose children are even smaller.<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week6/shift-down.jpg">

- **max-heapify**: Given an array A and an index i, assume the binary trees rooted at **left(i)** and **right(i)** are max heaps, but A[i] may be smaller than its children. Then the value at A[i] float down in the max-heap until the subtree rooted at index i becomes a max heap.<br>
<img src = "https://github.com/Xu-Yidi/fluteanzi/blob/master/week6/max-heapify.jpg">

- **build-max-heap**: We can use the max-heapify procedure to convert an array A[0,1,...,n-1] into a max-heap in a **bottom-up** manner. The elements in the subarray A[floor(n/2),...,n-1] are **leaves** of the tree, and so each is a 1-element heap. The procedure build-max-heap goes through the remaining nodes of the tree and runs max-heapify on each one.<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week6/build-max-heap1.jpg">
detailed process<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week6/build-max-heap2.jpg">
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week6/build-max-heap3.jpg">

### Heap Sort
- **Logic**<br>
1.Build a **max-heap** from the unorderes array<br>
2.Starting with the root(the maximum element), the algorithm places the maximum element into the correct place in the array by **swapping it with the element in the last position** in the array<br>
3.**"Discard" this last node**(knowing that it's in its correct place) by decreasing the heap size, and calling max-heapify on the new(possibly incorrectly-placed) root<br>
4.Repeating this "discarding" process until only one node(the smallest element) remains, and therefore is in the correct place in the array<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week6/heap_sort1.jpg">
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week6/heap_sort2.jpg">

- **Time Complexities**<br>
1.max-heapify:O(logn)<br>
2.build-max-heap:O(n)<br>
3.heap sort:O(nlogn)(best/worst/average case)<br>
[back to content](#content)<br>

## Week7
### Merge Sort
As quick sort, merge sort use recursion in an algorithm design called **divide-and-conquer**, so what's divide-and-conquer technique?<br>
- **Divide-and-conque**<br>
1.***Divide***: If the input size is smaller than a certain threshold(say, one or two element), solve the problem directly using a straightforward method and return the solution so obtained. Otherwise, divide the input data into two or more disjoint subsets<br>
2.***Conquer***: Recursively solve the subproblems associated with the subsets<br>
3.***Combine***: Take the solutions to the subproblems and merge them into a solution to the original problem<br>
- **Logic**<br>
To sort a sequence S with n elements using the three divide-and-coquer steps, the merge-sort algorithm proceeds as follows:<br>
1.***Divide***: If S has zero or one element, return S immediately; it is already sorted. Otherwise(S has at least two elements), remove all the elements from S and put them into two sequences, S1 and S2, each containing about half of the elements of; that is, S1 contaings the first *floor(n/2)* elements of S, and S2 contains the remaining *ceil(n/2)* elements<br>
2.***Conquer***: Recursively sort sequences S1 and S2<br>
3.***Combine***: Put back the elements into S by merging the sorted sequence S1 and S2 into a sorted sequence<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week7/merge_sort1.jpg">
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week7/merge_sort2.jpg">

- **Time Complexities**<br>
1.best case: O(nlogn)<br>
2.worst case:O(nlogn)<br>
3.average case:O(nlogn)<br>
[back to content](#content)<br>

## Week8
### Binary Tree
- **What's Binary Tree**<br>

A binary tree is an ordered tree with the following properties:<br>
>1.Every node has at most two children.<br>
>2.Each child node is labeled as being either a ***left child*** or a ***right child***.<br>
>3.A left child preceds a right child in the order of children of a node.<br>

The subtree rooted at a left or a right child of an internal node v is called a ***left subtree*** or ***right subtree***, respectively. A binary tree is ***proper*** or ***full*** if each node has either zero or two children. A binary tree that is not proper is ***improper***.<br>

- **Properties of Binary Tree**<br>

Let T be a nonempty binary tree, and let n, n<sub>E</sub>, n<sub>I</sub>, and h denote the number of nodes, number of external nodes, number of internal nodes, and height of T, respectively(a binary tree with height h has h+1 levels). Then T has the following properties:
>1.h + 1 ≤ n ≤ 2^h+1 - 1<br>
>2.1 ≤ n<sub>E</sub> ≤ 2^h<br>
>3.h ≤ n<sub>I</sub> ≤ 2^h - 1<br>
>4.log(n+1) - 1 ≤ h ≤ n - 1<br>

If T is proper, then T has the following properties:<br>
>1.2h + 1 ≤ n ≤ 2^h+1 - 1<br>
>2.h + 1 ≤ n<sub>E</sub> ≤ 2^h<br>
>3.h ≤ n<sub>I</sub> ≤ 2^h - 1<br>
>4.log(n+1) - 1 ≤ h ≤ (n-1)/2<br>
>5.n<sub>E</sub> = n<sub>I</sub> + 1<br>

- **The Binary Tree ADT**<br>
>**`T.left(p)`**: Return the position that represents the left child of p, or None if p has no left child<br>
>**`T.right(p)`**: Return the position that represents the right child of p, or None if p has no left child<br>
>**`T.sibling(p)`**: Return the position that represents the sibling of p, or None if p has no sibling<br>

- **Some Concepts**<br>

1.**Level**: The nodes in a binary tree are organized into ***levels*** with the root node at level 0, its children at level 1, the children of level one node are at level 2, and so on.<br>
>Example: tree(a) contains 2 nodes at level 1, 4 nodes at level 2, and 2 nodes at level 3.<br>

2.**Depth**: The ***depth*** of a node is its distance from the root, with distance being the number of levels that separate the two. A node's depth corresponds to the level it occupies.<br>
>Example: in tree(a), G has a depth of 2, in tree(b) it has a depth of 3, and in (c) its depth is 6.<br>

3.**Height**: The ***height*** of a binary tree is the number of edges between the tree's root and its furthest leaf.<br>
>Example: tree(a) has a height of 3, tree(b) has a height of 5, and tree(c) has a height of 7.<br>

4**Width**: The ***width*** of a binary tree is the number of nodes on the level containing the most node.<br>
>Example: tree(a) has a width of 4, tree(b) has a width of 3, and tree(3) has a width of 1.<br>

5.**Size**: The ***size*** of a binary tree is simply the number of nodes in the tree.<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week8/binary_tree1.jpg">

- **Tree Structures**<br>

1.**Full(improper) Binary Tree(完滿二元樹)**: A binary tree is a ***full binary tree*** if each node has either zero or two children, which means each interior node contains two children.
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week8/binary_tree2.jpg">

2.**Perfect Binary Tree(完美二元樹)**: A ***perfect binary tree*** is a full binary tree in which all leaf node are at the same level.
3.**Complete Binary Tree(完全二元樹)**: A binary tree of height h is a ***complete binary tree*** if it is a perfect binary tree down to height h-1 and the nodes on the lowest level fill the available slots from left to right leaving no gaps.<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week8/binary_tree3.jpg">

- **Tree Traversals**<br>

1.**Preorder traversal(前序)**: In preorder traversal, we first visit the node, and then traverse the nodes in its left subtree followed by the nodes in its right subtree. Since every node is the root of its own subtree, we can repeat the same process on each node, resulting in a recursive solution.<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week8/binary_tree4.jpg">

2.**Inorder traversal(中序)**: In inorder traversal, we first traverse the left subtree and then visit the node followed by the traversal of the right subtree.<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week8/binary_tree5.jpg">

3.**Postorder traversal(後序)**: In a postorder traversal, the left and right subtrees of each node are traversed before the node is visited.<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week8/binary_tree6.jpg">

[back to content](#content)<br>

## Week9
### Binary Search Tree(BST)
- A **binary search tree(BST)** is a binary tree in which each node contains a search key within its payload and the tree is structured such that for each interior node V:<br>
>1.All keys less than the key in node V are stored in the left subtree of V.<br>
>2.All keys greater than the key in node V are stored in the right subtree of V.<br>
- An **inorder traversal** of a binary tree visits positions in **increasing order** of their keys.<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week9/BST1.jpg">

### Basic Procedures
- **Searching**: If the target value is less than the root's key, we move left and we move right if it's greater. We repeat the comparision on the root node of the subtree and take the approriate path. This process is repeated until target is located or we encounter a null child link.<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week9/BST2.jpg">

- **Min/Max**: The minimum value can be located by starting at the root and following the left child links until a null link is encountered, and it means the minimum value will be found in a node that is either a leaf or an interior node with no left child. The maximum value can be found in a similar way.
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week9/BST3.jpg">

- **Insertions**: As the keys are inserted, a new node is created for each key and linked into its proper position within the tree. The new nodes are always inserted as a leaf nodes in its proper position such that the binary search tree property is maintained.<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week9/BST4.jpg">

- **Successor/Predecessor**: The successor(predecessor) of a key *k* in a search tree is the smallest(largest) key that belongs to the tree and that is strictly greater than(less than) *k*.<br>

1.The idea for finding the successor of a given node *k*:<br>
>(1)If *k* has the right child, then the successor is the minimum in the right subtree of *x*.<br>
>(2)Otherwise, the successor is the parent of the farthest node that can be reached from *x* by following only right branches backward.<br>

2.The idea for finding the predecessor of a given node *k*:<br>
>(1)If *k* has the left child, then the successor is the maximum in the left subtree of *x*.<br>
>(2)Otherwise, the successor is the parent of the farthest node that can be reached from *x* by following only left branches backward.<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week9/BST8.jpg">

- **Deletions**: An deletion involves searching for the node that contains the target key and then unlinking the node to remove it from the tree. When a node is removed, the remaining nodes must preserve the search tree property. Three cases should be consindered once the node has been located.<br>

1. The node *n* is a leaf: just replace *n* by null.<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week9/BST5.jpg">

2. The node *n* has a single child: promote the unique child to *n*'s place.<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week9/BST6.jpg">

3. The node *n* has two children:<br>
>(1)find the logical ***successor*** or ***predecessor***, *s*, of the node to be deleted, *n*<br>
>(2)copy the key from node *s* to node *n*<br>
>(3)remove node *s* from the tree<br>
<img src="https://github.com/Xu-Yidi/fluteanzi/blob/master/week9/BST7.jpg">

### Time Complexities

[back to content](#content)<br>

## Week10
