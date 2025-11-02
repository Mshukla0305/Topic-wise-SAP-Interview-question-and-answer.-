# Business Partner (BP) Master Data – SAP S/4HANA Interview Q&A

### Q1. What is a Business Partner in SAP S/4HANA?

A **Business Partner (BP)** is a single master record used to manage **customer, vendor, and contact person data** in one central place.

---

### Q2. Why did SAP replace Customer/Vendor Master with BP in S/4HANA?

To **unify data management** and **eliminate redundancy** — previously, customer and vendor masters were maintained separately in ECC.

---

### Q3. What is the main transaction code for BP?

**BP** — used to create, change, and display Business Partner master data.

---

### Q4. What are common BP roles?

* General Role (**000000**)
* Customer Roles (**FLCU00** – Company Code, **FLCU01** – Sales Area)
* Vendor Roles (**FLVN00 / FLVN01**)
* Contact Person (**000001**)

---

### Q5. Can one BP act as both a customer and vendor?

✅ Yes. You can assign both **Customer and Vendor roles** to the same BP.

---

### Q6. What is BP Grouping?

Defines **number range assignment** — internal or external numbering for Business Partners.

---

### Q7. Key BP tables:

* **BUT000** → General Data
* **BUT020** → Addresses
* **BUT100** → Roles

---

### Q8. What is the relationship between BP and Customer Master?

In **S/4HANA**, creating a BP with **Customer Role** automatically creates linked customer records in the background (**KNA1**, **KNVV**).

---

### Q9. How to extend BP to a new Sales Area?

Transaction **BP → Sales and Distribution Role (FLCU01)** → Add new **Sales Org + Distribution Channel + Division** data.

---

### Q10. What happens if BP is not extended to a Sales Area?

You **cannot create sales documents**, and the system will show:
❌ *“Customer not maintained for sales area”* error.

---

### Q11. How do you handle duplicate BPs during migration?

Use **BP relationship management**, manually merge duplicate data, and assign a **single number range** for migrated entries.

---

### Q12. What are BP roles configuration paths?

SPRO → Cross-Application Components → SAP Business Partner → Business Partner → Basic Settings → Business Partner Roles.

---

### Q13. What is the advantage of BP approach?

Centralized maintenance, **reduced redundancy**, and **integrated master data** across **SD, MM, and FI** modules.

---

 **Pro Tip:** Mastering BP configuration is essential in S/4HANA — it’s the foundation for smooth integration between sales, purchasing, and finance!
