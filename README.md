# Smallest-Number

```cpp
class Solution{
    static String smallestNumber(int S, int D){
        // code here
        StringBuilder op = new StringBuilder("");
        if(((double)S)/D <= 9){
            //sum achieved
            int temp = S -1;
            while(temp>0){
                if(temp>9){
                    temp-=9;
                    op.insert(0,'9');//prepend
                }
                else{
                    op.insert(0,((char)(temp+48)));
                    temp=0;
                }
            }
            while(op.length()<D){
                op.insert(0,'0');
            }
            op.replace(0,1,""+(char)(op.charAt(0)+1));//s-1--->s
            return op.toString();
        }
        else{
            return "-1";
        }
    }
}
```
Time Complexity : O(d)
