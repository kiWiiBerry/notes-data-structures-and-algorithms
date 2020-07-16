---
description: Depth First Search
---

# DFS

Use `Stack` to traverse the nodes.  

### 1. Inorder Traversal

* Iterative method:

```text
public List<Integer> inorderTraversal(TreeNode root) {
    List<Integer> result = new ArrayList<>();
    Stack<TreeNode> stack = new Stack<>();
    
    TreeNode curr = root;
    while (curr != null || !stack.isEmpty()){
        while (curr != null) {
            stack.push(curr);
            curr = curr.left;
        }
        
        curr = stack.pop();
        result.add(curr.val);     //---- process curr.value
        curr = curr.right;
    }
    
    return result;
}
```

* Recursive method:

```text
public List<Integer> inorderTraversal(TreeNode root) {
    List<Integer> res = new ArrayList<>();
    dfs(root, res);
    return res;
}

private void dfs(TreeNode node, List<Integer> res) {
    if (node != null) {
        dfs(node.left, ret);
        res.add(node.val);          //---- process node.val
        dfs(node.right, ret);
    }
}
```

### 

### 2. Pre-order Traversal

* Iterative method:

```text
public List<Integer> preorderTraversal(TreeNode root) {
    List<Integer> result = new ArrayList<>();
    if (root == null) return result;
    
    Stack<TreeNode> stack = new Stack<>();
    stack.push(root);
    
    while (!stack.isEmpty()) {
        TreeNode curr = stack.pop();
        
        result.add(curr.val);       //---- process curr.val
        
        if (curr.right != null) {
            stack.push(curr.right);
        }
        if (curr.left != null) {
            stack.push(curr.left);
        }
    }
    
    return result;
}
```

* Recursive method:

```text
public List<Integer> preorderTraversal(TreeNode root) {
    List<Integer> result = new ArrayList<>();
    preOrder(root, result);
    return result;
}

void preOrder(TreeNode node, List<Integer> list) {
    if (node == null) return;
    
    list.add(node.val);           //---- process node.val
    
    preOrder(node.left, list);
    preOrder(node.right, list);
}
```

### 

### 3. Post-order Traversal 

* Iterative method:

Use two `stack`. 

```text
public List<Integer> postorderTraversal(TreeNode root) {
    List<Integer> result = new ArrayList<>();
    
    Stack<TreeNode> tmp = new Stack<>();
    Stack<TreeNode> all = new Stack<>();
    
    if (root == null) return result;
    
    tmp.push(root);
    TreeNode curr;
    while (!tmp.isEmpty()) {
        curr = tmp.pop();
        all.push(curr);
        
        if (curr.left != null) tmp.push(curr.left);
        if (curr.right != null) tmp.push(curr.right);
    }
    
    while (!all.isEmpty()) {
        curr = all.pop();
        result.add(curr.val);          //---- process node.val     
    }
    
    return result;
}
```



* Recursive method:

```text
public List<Integer> postorderTraversal(TreeNode root) {
    List<Integer> result = new ArrayList<>();
    helper(result, root);
    return result;
}

public void helper(List<Integer> result, TreeNode node) {
    if (node == null) return;
    
    helper(result, node.left);
    helper(result, node.right);
    result.add(node.val);            //---- process node.val
}
```

