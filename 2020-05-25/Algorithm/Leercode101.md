#LeetCode 101 对称二叉树  
解题思路:通过递归把问题分解，核心思想就是判断左节点的left和右节点的right 以及左节点left是否为镜像节点，如果传入的参数都为null return false 如果其中一个不为空 return true。 看到网上还有深度遍历的解法，过于复杂 不如递归的思路简单。 
```
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public boolean isSymmetric(TreeNode root) {
            return root == null || isMirror(root.left, root.right);
        }

    public boolean isMirror(TreeNode L, TreeNode R) {
        if (L == null || R == null) {
            return L == R;
        }
        if (L.val != R.val) {
            return false;
        }
            return isMirror(L.left, R.right) && isMirror(L.right, R.left);
        }
}
```
