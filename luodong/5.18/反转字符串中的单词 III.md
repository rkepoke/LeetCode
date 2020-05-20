# [557. 反转字符串中的单词 III](https://leetcode-cn.com/problems/reverse-words-in-a-string-iii/)



### 代码实现


~~~java
class Solution {
    public String reverseWords(String s) {
        //存放最终的结果
        StringBuffer res = new StringBuffer();
        //根据空格分割成字符串数组
        String[] arrs = s.split(" ");
        //依次遍历，反转输入
        for(int i=0;i<arrs.length;i++){
            for(int j=arrs[i].length()-1;j>=0;j--){
                res.append(arrs[i].charAt(j));
            }
            if(i<arrs.length-1)
                res.append(" ");
        }
        return res.toString();
    }
}
~~~