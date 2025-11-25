
# 🚀 Province Count (Number of Connected Components) — DFS Solution

### **Java Code (Clean & Well-Formatted)**

```java
class Solution {

    public int findCircleNum(int[][] isConnected) {
        int n = isConnected.length;
        boolean[] visited = new boolean[n];
        int provinces = 0;

        for (int i = 0; i < n; i++) {
            if (!visited[i]) {
                dfs(i, visited, isConnected, n);
                provinces++;  // Found a new province
            }
        }
        return provinces;
    }

    private void dfs(int node, boolean[] visited, int[][] isConnected, int n) {
        visited[node] = true;

        for (int i = 0; i < n; i++) {
            // Only go to cities that are directly connected AND unvisited
            if (isConnected[node][i] == 1 && !visited[i]) {
                dfs(i, visited, isConnected, n);
            }
        }
    }
}
```

---

# 🧠 **Easy Explanation**

Socho tum **classroom** mein ho.

### 👥 Scenario:

* **Student 1** aur **Student 2** dost hain → donon ek **group** mein
* **Student 3** kisi se baat nahi karta → woh **akela group**

### ❓ To class mein kitne groups hue?

👉 **2 groups**, not 3.

Bilkul waise hi graph mein:

* 1 & 2 → connected → **one province**
* 3 → isolated → **second province**

---

# ⭐ Final Concept (Very Important)

### ✔ Connected cities = **same province**

### ✔ Isolated city = **separate province**

### ✔ “Province” = Connected component in the graph

---

# 🔍 Why not only `!visited[i]`?

* `!visited[i]` **sirf yeh batata hai** ki node visited nahi hua
* **Yeh nahi batata** ki dono nodes connected bhi hain ya nahi

### `isConnected[node][i] == 1`

* Yeh ensure karta hai ki **actual connection (edge)** hai

### Therefore:

✔ `isConnected[node][i] == 1` → confirms connection
✔ `!visited[i]` → confirms not visited yet

👉 **Dono condition lagana zaroori hai.**

---

If you want, I can generate a **GitHub-style README.md** file too!
