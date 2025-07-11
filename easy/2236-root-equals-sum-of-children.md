## 2236. Root Equals Sum of Children

You are given the `root` of **binary tree** that consistes of exactly `3` nodes: the root, its left child, and its right child.

Return `true` if the value of the root is equal to the **sum** of the values of its two children, or `false` otherwise.

### My pseudocode:

if (left side of the tree) + (right side of the tree) is equal to the head of the tree. Return true, else return false.

------

### C

#### My answer
```
bool checkTree(struct TreeNode* root) {
    if(root->left->val+root->right->val==root->val) {
        return true;
    }
    return false;
}
```

-----

### Python

#### My answer
```
class Solution(object):
    def checkTree(self, root):
        """
        :type root: Optional[TreeNode]
        :rtype: bool
        """
        # Check if left value + right value is equal to root value.
        return((root.left.val + root.right.val) == root.val)
```
