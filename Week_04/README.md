DP，动态规划，在还没有看教学之前觉得挺难的，看完之后也还会理解的不够深入
，然后就多看了两遍，慢慢的理解。
例如：最小路径和

class Solution {
    public int minPathSum(int[][] grid) {
   
    int m=grid.length;
    int n=grid[0].length;
    for(int i=0;i<m;i++){
     for(int j=0;j<n;j++){
    if(i == 0 && j == 0) continue;
    if(i==0){
      grid[i][j]= grid[0][j-1]+grid[i][j];
    }
    else if(j==0){
      grid[i][j]= grid[i-1][0]+grid[i][j];
    }else{
      grid[i][j]=Math.min(grid[i-1][j],grid[i][j-1]) + grid[i][j];
    }
     }
    }
    return grid[m-1][n-1];
    }
}
DP最重要的还是找到状态定义方程，如上面，grid[i][j]=Math.min(grid[i-1][j],grid[i][j-1]) + grid[i][j];
最终的思考还是回到最初：寻找重复性！已经将一个大问题如何转化为一个重复的更小的子问题。
这种跟二叉树的题的思想类似（考虑左右孩子），以及登山问题，最小路径问题，不同路径问题。。。
