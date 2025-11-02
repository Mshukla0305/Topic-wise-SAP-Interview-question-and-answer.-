# 🏗️ Enterprise Structure – SAP SD Interview Q&A

### Q1. What is Enterprise Structure in SAP?

It defines the **organizational framework** of a company in SAP — how legal and business units are structured.

---

### Q2. What are the key organizational units in SD?

* Sales Organization
* Distribution Channel
* Division
* Sales Office / Sales Group
* Plant (Logistics)
* Shipping Point

---

### Q3. How is Sales Area defined?

A **Sales Area** = Sales Organization + Distribution Channel + Division.

---

### Q4. What is the highest organizational unit in Sales?

**Sales Organization** is the highest unit.

---

### Q5. What is the link between Company Code and Sales Org?

* One **Company Code** → multiple **Sales Orgs** possible.
* One **Sales Org** → only one **Company Code**.

---

### Q6. Where do you assign Plant to Sales Org and Distribution Channel?

SPRO → Enterprise Structure → Assignment → SD → Assign Plant to Sales Org & Distribution Channel.

---

### Q7. How do you assign Shipping Point?

A **Shipping Point** is assigned to a **Plant** and determined based on **Delivery conditions**.

---

### Q8. What is Division in SAP SD?

Represents a **product line** or **product group** within an organization.

---

### Q9. What is the purpose of setting up common Distribution Channels and Divisions?

To enable **Cross-Division Sales** and allow data sharing across multiple channels/divisions.

---

### Q10. What is Sales Office and Sales Group?

Used for **reporting** and **responsibility assignment** within the Sales Organization.

---

### Q11. What are key tables related to Enterprise Structure?

* TVKO → Sales Organization
* TVKOV → Sales Area
* T001 → Company Code
* TVTW → Distribution Channel

---

### Q12. How is Enterprise Structure linked to Master Data?

**Sales Area**, **Company Code**, and **Plant** determine which data is fetched from **BP** and **Material Master**.

---

### Q13. Can one Plant belong to multiple Company Codes?

❌ No. Each Plant can belong to **only one Company Code.**

---

### Q14. What if Sales Org is not assigned to a Company Code?

**Financial postings will fail** during billing because accounting entries cannot be generated.

---

⭐ **Pro Tip:** Always ensure assignments in Enterprise Structure are consistent; otherwise, integration between SD, MM, and FI may break!
