# version-space

## **1. Introduction**

Version Space is a concept in Machine Learning that represents all hypotheses consistent with the training data. It is computed using the **Candidate Elimination Algorithm**, which maintains two boundaries:

* **S (Specific boundary)** – most specific hypothesis
* **G (General boundary)** – most general hypothesis

Version Space exists only when there is at least one hypothesis consistent with all training examples.

---

## **2. Situations Where Version Space is Impossible**

### **Case 1: Noisy Data (Contradictory Examples)**

When the same input produces different outputs, no single hypothesis can satisfy both.

**Example:**

* Sunny, Warm → Yes
* Sunny, Warm → No

**Reason:**
Contradiction leads to inconsistency, making the Version Space empty.

---

### **Case 2: Missing Attribute Values**

When some attribute values are unknown (represented as ‘?’), the algorithm cannot properly generalize or specialize.

**Example:**

* Sunny, ?, High → Yes

**Reason:**
Incomplete information prevents accurate hypothesis formation.

---

### **Case 3: Continuous Attributes**

Version Space works best with discrete attributes. Continuous values create infinite possibilities.

**Example:**

* Temperature = 30.5°C
* Temperature = 31.2°C

**Reason:**
Infinite hypothesis space makes it impossible to define clear S and G boundaries.

---

### **Case 4: Non-Deterministic Output**

When the same input leads to multiple valid outputs.

**Example:**

* Symptoms → Flu
* Same Symptoms → COVID

**Reason:**
Target concept is not fixed, so no consistent hypothesis exists.

---

### **Case 5: Large or Infinite Hypothesis Space**

When there are too many attributes or irrelevant features.

**Example:**

* Many unrelated attributes (color, size, ID, etc.)

**Reason:**
Computational complexity becomes too high, making Version Space impractical.

---

## **3. Conclusion**

Version Space can only be obtained when training data is:

* Consistent
* Complete
* Discrete
* Deterministic

In real-world scenarios, these conditions are often violated, making Version Space difficult or impossible to obtain.
