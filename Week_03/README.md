五毒神掌（覃超老师）：

第一遍：五分钟读题思考，有思路就直接写，没思路就直接看题解并默写题解
第二遍：不看题解，自己写代码
第三遍：24小时后
第四遍：一周后
第五遍：面试前

关于使用HashMap的经典题目：
多数元素：
 public int majorityElement(int[] nums) {
    HashMap<Integer ,Integer >mp=new HashMap();
    for(int st:nums){
      if(!mp.containsKey(st)){
        mp.put(st,1);
      }
        mp.put(st,mp.get(st)+1);
    }
    int sum=0;
    int key=0;
    //循环出最大的值，获取key
    for(Map.Entry<Integer,Integer> sk:mp.entrySet()){
        if(sk.getValue()>sum){
            sum=sk.getValue();
            key=sk.getKey();
        }
    }
     return key;
    }
    总结：一般如果一个数组中有多个元素，并且要使用到多个元素或者比较个数之类的题目，
    可以考虑使用map,因为它是key-value的形式保持数据。通过containskey可以看map中
    是否已经有这个元素，通过map.entrySet()方法，查看key-value
   
    回溯法：个人总结
    基本和递归是一样的，只是多了一个剪枝的步骤，回溯的精髓是，下探看看是否符合，如果不符合
    要求那个就返回上一层继续，在刚开始不熟悉的情况下，最好画出递归树。
    
    如求子集：
    List<List<Integer>> res=new ArrayList();
    public List<List<Integer>> subsets(int[] nums) {
      backtry(nums,new ArrayList(),0);
      return res;
    }
    public void backtry(int[] nums,ArrayList<Integer> List,int first) {
     res.add(new ArrayList(List));
     for(int i=first;i<nums.length;i++){
       List.add(nums[i]);
       backtry(nums,List,i+1);
       List.remove(List.size()-1);
     }
    }
    
    
    
    
