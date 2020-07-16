---
description: Breadth First Search
---

# BFS

#### Classic Problem:

LC102: [Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/) 

```text
public List<List<Integer>> levelOrder(TreeNode root) {
    List<List<Integer>> result = new ArrayList<>();
    Queue<TreeNode> queue = new LinkedList<>();

    if (root == null) return result;

    queue.add(root);
    while (!queue.isEmpty()) {
        int size = queue.size();
        List<Integer> levelList = new ArrayList<>();
        for (int i = 0; i < size; i++) {
            TreeNode curr = queue.poll();
            levelList.add(curr.val);

            if (curr.left != null) queue.add(curr.left);
            if (curr.right != null) queue.add(curr.right);
        }
        result.add(levelList);
    }
    return result;
}
```



{% hint style="info" %}
1. Use a queue to store all the nodes. When the queue is empty, all nodes are visited.
2. Inside the while loop, use a for loop to traverse each level and add the child nodes to the queue.
{% endhint %}

#### More similar questions:

1. LC103, [Binary Tree Zigzag Level Order Traversal ](https://leetcode.com/problems/binary-tree-zigzag-level-order-traversal/)

