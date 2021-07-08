# 从尾到头打印链表
## 输入一个链表的头节点，从尾到头反过来返回每个节点的值（用数组返回）。
### 例子：输入：head[1,2,3],输出[2,3,1]
ps:链表长度大于0，小于10000.
### 代码
class Solution{

    public int[] reversePrint(ListNode head){
        Stack<ListNode> s = new Stack();
        ListNode temp = head;
        while(temp != null ){
            s.push(temp);
            temp = temp.next;
        }
        int size = s.size();
        int[] arr = new int[size];
        for (int i = 0;i < size; i++){
            arr[i] = s.pop().val;
        }
        return arr;
    }
}