# nth-element-from-2nd-last
package LinkedList;

public class nthnodefrom2ndlast {

    // 2nd last
    public static Node nthNode(Node head,int n){
        Node slow=head;
        Node fast=head;
        for(int i=1;i<=n;i++){
            fast=fast.next;
        }
        while(fast!=null){
            slow=slow.next;
            fast=fast.next;
        }
        return slow;
    }
    public static class Node{
        int data;
        Node next;
        Node(int data) {
            this.data = data;
        }
    }
    public static void main(String[] args) {
        Node a=new Node(100);
        Node b=new Node(13);
        Node c=new Node(12);
        Node d=new Node(4);
        Node e=new Node(5);
        Node f=new Node(10);
        a.next=b;
        b.next=c;
        c.next=d;
        d.next=e;
        e.next=f;
        Node q=nthNode(a,4);
        System.out.println(q.data);


    }
}


