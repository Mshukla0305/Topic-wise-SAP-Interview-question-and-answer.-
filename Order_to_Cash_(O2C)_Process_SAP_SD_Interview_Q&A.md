# Order to Cash (O2C) Process – SAP SD Interview Q&A

### Q1. What is O2C in SAP?

Order to Cash is the **end-to-end sales cycle** from customer inquiry to payment receipt.

---

### Q2. What are the main steps in O2C?

**Inquiry → Quotation → Sales Order → Delivery → Billing → Payment**

---

### Q3. What is the T-code to create a Sales Order?

**VA01**

---

### Q4. How is Availability Check performed?

Based on **Material Master, MRP, and ATP logic** during order creation.

---

### Q5. What is Copy Control?

Defines how data flows between sales documents (e.g., **Quotation → Order → Delivery → Billing**).

---

### Q6. What is a Delivery Document?

It triggers **Goods Issue** and updates inventory; created via **VL01N**.

---

### Q7. What happens at Goods Issue?

* Stock decreases
* Accounting entries are posted (**COGS and Inventory**)
* Document flow updates

---

### Q8. What is a Billing Document?

Represents the **invoice to the customer**, generated via **VF01**.

---

### Q9. What are accounting entries at billing?

* **Customer Account (Debit)**
* **Revenue Account (Credit)**

---

### Q10. What is Document Flow?

Tracks all related documents in a sales process (**Order → Delivery → Invoice**).

---

### Q11. What is Pricing Procedure?

Defines how system calculates **prices, discounts, surcharges, and taxes** in an order.

---

### Q12. What controls Item Category determination?

**Sales Document Type + Item Category Group + MRP Type + Higher-Level Item**

---

### Q13. What controls Schedule Line Category?

**Item Category + MRP Type** combination.

---

### Q14. What is Credit Management in O2C?

Checks **customer credit limit** before order or delivery creation.

---

### Q15. How are incompletion logs used?

Identify **missing mandatory fields** in documents (header/item level).

---

### Q16. What happens after posting the invoice in O2C?

Accounting entries are sent to **FI**, **AR updated**, then payment is applied via **F-28** or auto-clearing.

---

### Q17. What is ATP Check?

**Available-to-Promise** check ensures stock availability during order creation.

---

### Q18. How is Delivery Block or Billing Block used?

Used to **hold orders** for approval or pending master data validations.

---

### Q19. What is Output Determination in Billing?

Controls how **invoice output (print/email)** is triggered via **condition technique**.

---

### Q20. What tables are involved in O2C?

* VBAK → Sales Order Header
* VBAP → Sales Order Item
* LIKP → Delivery Header
* LIPS → Delivery Item
* VBRK → Billing Header
* VBRP → Billing Item

---

 **Pro Tip:** A strong grasp of O2C shows not only your SD knowledge but also your understanding of integration with MM and FI modules!
