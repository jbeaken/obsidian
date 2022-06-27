[[Data Structures]]

A **binary tree** is a [tree data structure](https://en.wikipedia.org/wiki/Tree_(data_structure) "Tree (data structure)") in which each node has at most two [children](https://en.wikipedia.org/wiki/Child_node "Child node"), which are referred to as the _left child_ and the _right child_.





-   **Root:** The root of a tree is the topmost node of the tree that has no parent node. There is only one root node in every tree.
-   **Edge:** Edge acts as a link between the parent node and the child node.
-   **Leaf:** A node that has no child is known as the leaf node. It is the last node of the tree. There can be multiple leaf nodes in a tree.
-   **Depth:** The depth of the node is the distance from the root node to that particular node.
-   **Height:** The height of the node is the distance from that node to the deepest node of the tree.
-   **Height of tree:** The Height of the tree is the maximum height of any node.

```java
class Node {
    int key;
    Node left, right;
 
    public Node(int item) {
        key = item;
        left = right = null;
    }
}
```

[[Binary Tree Traversals]]
[[Binary Tree Insertion]]
[[Kotlin Binary Tree]]

References
[https://www.geeksforgeeks.org/binary-tree-data-structure/?ref=lbp](https://www.geeksforgeeks.org/binary-tree-data-structure/?ref=lbp)