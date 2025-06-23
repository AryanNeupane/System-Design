
# 🧠 Low-Level Design (LLD) Explained

## 1. What is Low-Level Design?

> **Definition**: Low-Level Design (LLD) is the process of defining the internal structure of an application — its *skeleton* — by identifying classes, objects, their relationships, data flow, and how algorithmic solutions (DSA) are integrated into this structure.

### Difference from DSA:

| Concept                                | Description                                                                                                                      |
| -------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **DSA (Data Structures & Algorithms)** | Solves specific, isolated problems using techniques like binary search, quicksort, Dijkstra’s, heaps, etc.                       |
| **LLD**                                | Structures the entire system — defines objects and how they interact, and then integrates appropriate DSA within this framework. |

---

## 2. 🚖 Illustrative Story: Building “QuickRide” (Uber/Ola Clone)

### 🧠 Anurag’s *DSA-First* Approach:

1. Problem Decomposition:

   * Model city intersections as **graph nodes**, roads as **edges**.
   * Use **Dijkstra’s algorithm** to find shortest routes.
   * Use **min-heap** for matching closest drivers.
2. Gaps in this approach:

   * ❌ No definition of entities like `User`, `Rider`, `Location`, `Notification`, `Payment`.
   * ❌ Ignores non-functional concerns like **data security** (e.g., phone masking).
   * ❌ Lacks integration components: payment gateway, notifications, scaling strategy.

### 🏗️ Maurya’s *LLD-First* Approach:

1. **Entity Identification**:

   * Key classes: `User`, `Rider`, `Location`, `NotificationService`, `PaymentGateway`, etc.
2. **Define Interactions**:

   * E.g., how `User` interacts with `Rider` through `Location`, how services like `NotificationService` and `PaymentGateway` are integrated.
3. **Non-Functional Design**:

   * 🔐 Data Security
   * ⚙️ Scalability
4. **Then Integrate DSA**:

   * Embed Dijkstra’s and driver-matching algorithms *inside* the class design.

---

## 3. 🎯 Core Principles of LLD

| Principle           | Description                                                                                       |
| ------------------- | ------------------------------------------------------------------------------------------------- |
| **Scalability**     | System should support millions of users without performance bottlenecks.                          |
| **Maintainability** | Easy to extend and debug; new features shouldn’t break old ones.                                  |
| **Reusability**     | Modular, loosely coupled design — e.g., reusable notification/matching services across platforms. |

---

## 4. 🔄 LLD vs. HLD

| Design Level                | Focus                                                                                            |
| --------------------------- | ------------------------------------------------------------------------------------------------ |
| **LLD (Low-Level Design)**  | Internal structure, object modeling, class design, data flow, code layout                        |
| **HLD (High-Level Design)** | Overall architecture — tech stack, databases, server scaling, deployment strategies, cloud costs |

### HLD covers:

* 🧱 Tech stack: Java, Spring Boot, Node.js, etc.
* 🗃️ Database: SQL, NoSQL, hybrid
* ☁️ Deployment: AWS/GCP, autoscaling, load balancing
* 💰 Cost optimization

---

## 5. ✅ Summary & Takeaways

* **DSA** = The **brain** of your app: solves specific problems.
* **LLD** = The **skeleton**: defines objects, their structure, relationships, and where to apply DSA.
* **HLD** = The **architecture**: system-wide infrastructure, deployment, scaling.

---

## 6. 🔑 Key Line to Remember

> 🧠 *"If DSA is the brain, LLD is the skeleton of your application."*





