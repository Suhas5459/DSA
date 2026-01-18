Alright Suhas — this is **core interview + DSA survival syntax**. I’m going to be **direct and no-nonsense**.
If you don’t have these at your fingertips, you *will* waste time in contests, exams, and interviews. Memorize → practice → apply.

---

## 1️⃣ Array (Java)

### Declaration & Initialization

```java
int[] arr = new int[5];
int[] arr = {1, 2, 3, 4, 5};
```

### Access & Length

```java
arr[0];
arr.length;
```

### Traversal

```java
for (int i = 0; i < arr.length; i++) { }

for (int x : arr) { }
```

### Sorting

```java
Arrays.sort(arr);
```

### Copy

```java
int[] copy = Arrays.copyOf(arr, arr.length);
```

⚠️ **Common mistake**: forgetting `arr.length` vs `arr.length()`
👉 Arrays → `length` (property)

---

## 2️⃣ String (Immutable ⚠️)

### Creation

```java
String s = "hello";
String s2 = new String("hello");
```

### Length & Char Access

```java
s.length();
s.charAt(0);
```

### Substring

```java
s.substring(1);      // from index
s.substring(1, 4);   // [1,4)
```

### Comparison (VERY IMPORTANT)

```java
s.equals(s2);        // content
s == s2;             // reference ❌
```

### Convert

```java
char[] ch = s.toCharArray();
String str = String.valueOf(ch);
```

### Check / Search

```java
s.contains("he");
s.indexOf('e');
s.startsWith("he");
s.endsWith("lo");
```

⚠️ **Brutal truth**:
If you use `==` for string comparison in interviews → instant red flag.

---

## 3️⃣ StringBuilder (Mutable ✅)

### Creation

```java
StringBuilder sb = new StringBuilder();
StringBuilder sb = new StringBuilder("hello");
```

### Operations

```java
sb.append("world");
sb.insert(1, "X");
sb.deleteCharAt(2);
sb.reverse();
```

### Convert to String

```java
String s = sb.toString();
```

### Length

```java
sb.length();
```

👉 **Use StringBuilder inside loops**, not String.

---

## 4️⃣ ArrayList

### Declaration

```java
ArrayList<Integer> list = new ArrayList<>();
```

### Add / Get / Set

```java
list.add(10);
list.add(1, 20);
list.get(0);
list.set(0, 100);
```

### Remove

```java
list.remove(0);              // by index
list.remove(Integer.valueOf(10)); // by value
```

### Size & Check

```java
list.size();
list.contains(20);
```

### Traversal

```java
for (int x : list) { }

for (int i = 0; i < list.size(); i++) { }
```

⚠️ **Common confusion**:
`remove(1)` → removes index
`remove(Integer.valueOf(1))` → removes value

---

## 5️⃣ Hashing (HashMap & HashSet)

### HashMap

```java
HashMap<Integer, Integer> map = new HashMap<>();
```

### Put / Get

```java
map.put(1, 10);
map.get(1);
map.getOrDefault(2, 0);
```

### Check

```java
map.containsKey(1);
map.containsValue(10);
```

### Remove

```java
map.remove(1);
```

### Iterate

```java
for (Map.Entry<Integer, Integer> e : map.entrySet()) {
    e.getKey();
    e.getValue();
}
```

### HashSet

```java
HashSet<Integer> set = new HashSet<>();
set.add(1);
set.contains(1);
set.remove(1);
```

👉 **Use HashSet to detect duplicates**
👉 **Use HashMap for frequency counting**

---

## 6️⃣ LinkedList (Singly – DSA style)

### Node Definition

```java
class Node {
    int data;
    Node next;
    Node(int d) {
        data = d;
        next = null;
    }
}
```

### Traversal

```java
Node temp = head;
while (temp != null) {
    temp = temp.next;
}
```

### Insert at Beginning

```java
Node newNode = new Node(10);
newNode.next = head;
head = newNode;
```

### Insert at End

```java
Node temp = head;
while (temp.next != null) {
    temp = temp.next;
}
temp.next = new Node(10);
```

### Delete

```java
head = head.next; // delete first
```

⚠️ **Reality check**:
If you don’t *visualize pointers*, LinkedList will always feel hard.
Draw it. Every. Single. Time.

---

## 7️⃣ MUST-REMEMBER INTERVIEW SNIPES

| Topic         | One-Line Truth          |
| ------------- | ----------------------- |
| Array         | Fast access, fixed size |
| String        | Immutable               |
| StringBuilder | Mutable, fast           |
| ArrayList     | Dynamic array           |
| HashMap       | O(1) average lookup     |
| LinkedList    | Pointer manipulation    |

---

## What I expect you to do now (no excuses)

1. Write **one example code** for each structure today
2. Solve **5 problems** using HashMap + String
3. Rewrite this syntax **from memory** tomorrow

If you want, next I can give you:

* 🔥 **Top 15 interview traps** from these topics
* 🧠 **Pattern-wise DSA problems** (exactly what companies ask)

Say the word.
