public class MmustLinkedList {
    private class Node {
        private int data;
        private Node next;

        public Node(int data) {
            this.data = data;
            this.next = null;
        }
    }

    private Node head;
    private Node tail;
    private int size;

    public MmustLinkedList() {
        head = null;
        tail = null;
        size = 0;
    }

    public boolean isEmpty() {
        return size == 0;
    }

    public void addFirst(int data) {
        Node new_node = new Node(data);
        if (isEmpty()) {
            head = new_node;
            tail = new_node;
        } else {
            new_node.next = head;
            head = new_node;
        }
        size++;
    }

    public void addLast(int data) {
        Node new_node = new Node(data);
        if (isEmpty()) {
            head = new_node;
            tail = new_node;
        } else {
            tail.next = new_node;
            tail = new_node;
        }
        size++;
    }

    public int removeFirst() {
        if (isEmpty()) {
            throw new RuntimeException("List is empty");
        }
        Node removed_node = head;
        if (head == tail) {
            head = null;
            tail = null;
        } else {
            head = removed_node.next;
        }
        size--;
        return removed_node.data;
    }

    public int removeLast() {
        if (isEmpty()) {
            throw new RuntimeException("List is empty");
        }
        Node removed_node = tail;
        if (head == tail) {
            head = null;
            tail = null;
        } else {
            Node current_node = head;
            while (current_node.next != tail) {
                current_node = current_node.next;
            }
            current_node.next = null;
            tail = current_node;
        }
        size--;
        return removed_node.data;
    }

    public int size() {
        return size;
    }

    @Override
    public String toString() {
        if (isEmpty()) {
            return "List is empty";
        }
        Node current_node = head;
        StringBuilder nodes = new StringBuilder();
        while (current_node != null) {
            nodes.append(current_node.data);
            if (current_node.next != null) {
                nodes.append("->");
            }
            current_node = current_node.next;
        }
        return nodes.toString();
    }
}
