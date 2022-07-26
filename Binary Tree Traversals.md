q
![Alt Test](https://media.geeksforgeeks.org/wp-content/cdn-uploads/2009/06/tree12.gif)

Depth First Traversals:   

(a) Inorder (Left, Root, Right) : 4 2 5 1 3   
(b) Preorder (Root, Left, Right) : 1 2 4 5 3   
(c) Postorder (Left, Right, Root) : 4 5 2 3 1  

Breadth-First or Level Order Traversal: 1 2 3 4 5   
Please see [this](https://www.geeksforgeeks.org/level-order-tree-traversal/) post for Breadth-First Traversal.

[Baeldung](https://www.baeldung.com/java-depth-first-search)

Both algorithms may come in two variants: [Tree-Like Search and Graph Search](https://www.baeldung.com/cs/graph-search-vs-tree-like-search).

[Difference Between BFS and DFS](https://www.baeldung.com/cs/dfs-vs-bfs)

```java
// Java program for different tree traversals

/* Class containing left and right child of current
node and key value*/
class Node {
	int key;
	Node left, right;

	public Node(int item) {
		key = item;
		left = right = null;
	}
}

class BinaryTree {
	// Root of Binary Tree
	Node root;

	BinaryTree() { root = null; }

	/* Given a binary tree, print its nodes according to the
	"bottom-up" postorder traversal. */
	void printPostorder(Node node)	{
		if (node == null) return;

		// first recur on left subtree
		printPostorder(node.left);

		// then recur on right subtree
		printPostorder(node.right);

		// now deal with the node
		System.out.print(node.key + " ");
	}

	/* Given a binary tree, print its nodes in inorder*/
	void printInorder(Node node) {
		if (node == null) return;

		/* first recur on left child */
		printInorder(node.left);

		/* then print the data of node */
		System.out.print(node.key + " ");

		/* now recur on right child */
		printInorder(node.right);
	}

	/* Given a binary tree, print its nodes in preorder*/
	void printPreorder(Node node) {
		if (node == null) return;

		/* first print data of node */
		System.out.print(node.key + " ");

		/* then recur on left subtree */
		printPreorder(node.left);

		/* now recur on right subtree */
		printPreorder(node.right);
	}

	// Wrappers over above recursive functions
	void printPostorder() { printPostorder(root); }
	void printInorder() { printInorder(root); }
	void printPreorder() { printPreorder(root); }

	// Driver method
	public static void main(String[] args)
	{
		BinaryTree tree = new BinaryTree();
		tree.root = new Node(1);
		tree.root.left = new Node(2);
		tree.root.right = new Node(3);
		tree.root.left.left = new Node(4);
		tree.root.left.right = new Node(5);

		System.out.println(
			"Preorder traversal of binary tree is ");
		tree.printPreorder();

		System.out.println(
			"\nInorder traversal of binary tree is ");
		tree.printInorder();

		System.out.println(
			"\nPostorder traversal of binary tree is ");
		tree.printPostorder();
	}
}

```