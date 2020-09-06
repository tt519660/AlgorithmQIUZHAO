 五毒神掌：

第一遍：五分钟读题思考，有思路就直接写，没思路就直接看题解并默写题解 
第二遍：不看题解，自己写代码 
第三遍：24小时后
第四遍：一周后
第五遍：面试前

二叉树的遍历：
前序遍历：根左右
中序遍历：左根右
后序遍历：左右根


例如：前序遍历：根左右，可以使用数组的方式，简单来看就是根对应添加节点，左右节点则使用递归
public List<Integer> inOrderTree (TreeNode root,List li){
    if(root!=null){
        li.add(root.val);
      if(root.left!=null){
      inOrderTree(root.left,li);
      }
    if(root.right!=null){
      inOrderTree(root.right,li);
      }
    }
  
  个人感悟：
  关于二叉树，不要使用机械的方式思考，要寻找重复性，大部分的树的问题是都可以使用递归，例如：树的求树的深度，
  树的遍历，并且首先考虑使用递归的方式去求解。
