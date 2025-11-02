# Master Data (Customer, Material, Pricing, etc.) – SAP SD Interview Q&A

### Q1. What is Master Data in SAP SD?

**Master Data** is the core data that doesn’t change frequently — it includes **Customer**, **Material**, **Pricing**, **Output**, and **Credit Master** data used across processes.

---

### Q2. What are key types of Master Data in SD?

* Customer Master
* Material Master
* Pricing Conditions
* Output Master
* Credit Master

---

### Q3. What are Customer Master segments?

* **General Data** → KNA1
* **Company Code Data** → KNB1
* **Sales Area Data** → KNVV

---

### Q4. What are the main views in Material Master for SD?

* **Sales Org 1 View**
* **Sales Org 2 View**
* **Sales: General/Plant Data View**

---

### Q5. What determines whether a customer can create orders or billing?

**Account Group** and **BP Role (FLCU01)** determine the capability to create **Sales Orders** and **Billing Documents**.

---

### Q6. What is the link between Material Master and Division?

Each **Material** is assigned to a **Division**, which helps in **Sales Area determination**.

---

### Q7. What is a Condition Record?

A **Pricing Master Data entry** containing specific price, discount, or tax conditions for defined keys (e.g., Customer, Material, Sales Org).

---

### Q8. What tables store pricing data?

* **KONV** → Transaction-level conditions
* **Axxx tables** → Condition records (A004, A305, etc.)

---

### Q9. What is Output Master?

Defines **Output Types** (Invoice print, Email, EDI, etc.) and their determination in **Sales Documents**.

---

### Q10. What is Customer Account Group?

Controls **field selection**, **number range**, and defines **customer type** (Sold-to, Ship-to, Bill-to, Payer).

---

### Q11. Can multiple customers share the same Sales Area?

✅ Yes, as long as they belong to the **same Sales Org**, **Distribution Channel**, and **Division**.

---

### Q12. What happens if Material Master is missing Sales Org data?

You cannot create **Sales Orders** — system will show:
❌ *“Material not maintained for Sales Org/Dist Channel.”*

---

### Q13. What determines Tax Classification?

Combination of **Customer Master Tax Data + Material Master Tax Data** through **Access Sequence** in the **Pricing Procedure**.

---

### Q14. What is Partner Determination?

Defines which **Business Partners** (Sold-to, Ship-to, Bill-to, Payer) are mandatory for specific sales documents.

---

### Q15. Where do you maintain Customer Hierarchies?

Transaction **VCH1** or via **BP Relationships** in S/4HANA.

---

 **Pro Tip:** Always ensure Master Data consistency across modules — it’s the backbone of every O2C and integration process in SAP!
