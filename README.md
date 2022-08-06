# Binary Tree Traversal
Set of programming assignments that are designed to test knowledge of traversal methods for binary trees.

### Basic data structure for representing binary trees

You may assume that for all programming assignments within this problem set the following data class
will be used to represent tree nodes:

```python
class TreeNone:
    def __init__(
        self,
        value: int = 0,
        left: Optional['TreeNone'] = None,
        right: Optional['TreeNone'] = None
    ):
        self.value = value
        self.left = left
        self.right = right
```

The implementation above can be found within `tasks/binary_tree_node.py` file.

For example the following tree could be created using the snippet below:


```mermaid
graph TD;
    A[2]-->B[4];
    A-->C[9];
```

```python
b = TreeNode(value=4)
c = TreeNode(value=9)
a = TreeNode(value=2, left=b, right=c)
```

## Problem 1: Check whether two trees are the same

Given the roots of two binary trees `p` and `q`, write a function to check if they are the same or not.

Two binary trees are considered the same if they are structurally identical, and the nodes have the same value.

**Example 1:**
```mermaid
graph BR;
    subgraph Q
    A((1))-->B((2))
    A-->C((3))
    end
    subgraph P
    AA((1))-->BB((2))
    AA-->CC((3))
    end  
```

Expected result: True.

**Example 2:**
```mermaid
graph BR;
    subgraph Q
    A((1))-->B((3))
    A-->C((2))
    end
    subgraph P
    AA((1))-->BB((2))
    AA-->CC((3))
    end  
```

Expected result: False.

**Example 3:**
```mermaid
graph BR;
    subgraph Q
    A((1))-->B((3))
    A-->C((2))
    C-->D((5))
    C-->F((None))
    end
    subgraph P
    AA((1))-->BB((3))
    AA-->CC((2))
    end  
```

Expected result: False.

Please use a template for the implementation (`tasks/binary_tree_comparison:check_trees_equality`).


## Problem 2: Get inorder traversal of binary tree

Given the `root` of a binary tree, return the inorder traversal of its nodes' values.

**Example:**
```mermaid
graph BR;
    A((20))-->B((13))
    A-->C((7))
    B-->D((2))
    B-->E((14))
    C-->F((12))
    C-->G((None))
```

Expected result: [2, 13, 14, 20, 12, 7].

Please use a template for the implementation (`tasks/binary_tree_traversal:get_inorder_traversal`).


## Problem 3: Get postorder traversal of binary tree

Given the `root` of a binary tree, return the postorder traversal of its nodes' values.

**Example:**
```mermaid
graph BR;
    A((20))-->B((13))
    A-->C((7))
    B-->D((2))
    B-->E((14))
    C-->F((12))
    C-->G((None))
```

Expected result: [2, 14, 13, 12, 7, 20].

Please use a template for the implementation (`tasks/binary_tree_traversal:get_postorder_traversal`).


## Problem 4: Get preorder traversal of binary tree

Given the `root` of a binary tree, return the preorder traversal of its nodes' values.

**Example:**
```mermaid
graph BR;
    A((20))-->B((13))
    A-->C((7))
    B-->D((2))
    B-->E((14))
    C-->F((12))
    C-->G((None))
```

Expected result: [20, 13, 2, 14, 7, 12].

Please use a template for the implementation (`tasks/binary_tree_traversal:get_preorder_traversal`).


## Problem 5: Get level order traversal of binary tree

Given the `root` of a binary tree, return the level order traversal of its nodes' values. (i.e., from left to right, level by level).

**Example:**
```mermaid
graph BR;
    A((20))-->B((13))
    A-->C((7))
    B-->D((2))
    B-->E((14))
    C-->F((12))
    C-->G((None))
```

Expected result: [20, 13, 7, 2, 14, 12].

Please use a template for the implementation (`tasks/binary_tree_traversal:get_level_order_traversal`).
