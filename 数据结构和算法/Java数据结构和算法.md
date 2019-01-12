### 一、链表

#### 1.1 求单链表中结点的个数

求链表中结点个数,注意检查链表是否为空，时间复杂度O(n)。

```java
public class LinkNode {
    int value;
    LinkNode next;
    public LinkNode(int value) {
        super();
        this.value = value;
        this.next = null;
    }

    public static int getListLength(LinkNode root) {    //一定要加static，调用方法时使用LinkNode.getListLength
        int result = 0;
        if(root == null)
            return result;
        LinkNode cursor = root;
        while(cursor!=null){
            result++;
            cursor = cursor.next;
        }
        return result;
    }
}
```

```java
public class Main {
    public static void main(String[] args) {
        LinkNode a = new LinkNode(1);
        System.out.println(LinkNode.getListLength(a));
    }
}
```

