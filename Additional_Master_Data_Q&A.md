# 💼 SAP SD — Additional Master Data Topics

### 🎯 Interview Questions and Answers

---

## 🧩 **1️⃣ Common Master Data – Distribution Channels**

**Q1. What is a distribution channel in SAP SD?**
A: A distribution channel shows how products or services reach customers — like retail, online, or wholesale.

**Q2. What is the purpose of a representative distribution channel?**
A: To use one set of master data across multiple channels, saving time and reducing effort.

**Q3. Benefits of representative distribution channels?**

* Less data maintenance
* Faster setup
* Easier reporting

**Q4. Where is it configured?**
A: SPRO → Enterprise Structure → Assignment → Sales & Distribution → Master Data → Define Common Distribution Channels.

**Q5. Can one representative channel serve multiple sales orgs?**
A: No, it is valid only within one sales organization.

---

## 🏗️ **2️⃣ Common Master Data – Divisions**

**Q6. What is a division in SAP SD?**
A: A division represents a product line or category like electronics, furniture, etc.

**Q7. Why create a representative division?**
A: To share the same master data across multiple divisions and reduce redundancy.

**Q8. Benefits?**

* Less time maintaining master data
* Simplified reporting
* Easy data management

**Q9. Where is it configured?**
A: SPRO → Enterprise Structure → Assignment → Sales & Distribution → Master Data → Define Common Divisions.

---

## 📤 **3️⃣ Output Master Data**

**Q10. What is Output Master Data?**
A: It controls how SAP sends documents (like invoices or order confirmations) via print, email, fax, or EDI.

**Q11. Common output types?**

* Order confirmation
* Delivery note
* Invoice
* Quotation

**Q12. Classical vs. S/4HANA Output Management?**

* Classical: Uses condition technique.
* S/4HANA: Uses BRF+ (Business Rule Framework Plus), integrated with Fiori.

**Q13. Advantages of S/4HANA Output Management:**

* Works across SD, MM, FI
* Flexible email settings
* Multi-recipient support
* Fiori integration

**Q14. Transaction for batch outputs?**
A: RSNAST00

**Q15. Output channels in S/4HANA:**

* Print
* Email
* XML
* IDoc (on-premise)

---

## 📋 **4️⃣ Item Proposals**

**Q16. What is an item proposal?**
A: A pre-defined list of products that a customer frequently orders.

**Q17. Benefits:**

* Saves time
* Auto-fills recurring order items

**Q18. Transaction code to create?**
A: VD51

**Q19. How to assign an item proposal to a customer?**
A: In customer master → Sales Area Data → Sales Tab → Enter item proposal number.

**Q20. Can you change items while ordering?**
A: Yes, you can modify or remove items.

**Q21. Typical use cases:**

* Regular repeat orders
* Opening product suggestions

---

## 🧾 **5️⃣ Incompleteness Check**

**Q22. Purpose of incompleteness check?**
A: Ensures all required fields are filled before delivery or billing.

**Q23. What if a document is incomplete?**
A: SAP shows a warning, may block follow-up processes, or allow saving with errors.

**Q24. Transaction to define procedures?**
A: VOFM → Incompleteness Procedures

**Q25. What data is checked?**

* Header data (customer PO)
* Item data (material number)
* Partner data (ship-to party)

**Q26. How to fix incomplete data?**
A: Open Incompletion Log → Fill missing values.

**Q27. Can an incomplete doc be saved?**
A: Yes, depending on configuration.

---

## 🧠 **Bonus Questions**

**Q28. Relation between master data and transactions?**
A: Master data provides base info (like customers, materials, prices) for transactions like sales orders.

**Q29. Why is master data maintenance important?**
A: Wrong or missing master data causes sales and billing errors.

**Q30. How does SAP maintain consistency across channels/divisions?**
A: By using representative channels/divisions that share master data.

---

✅ Total: 30 Questions & Answers — Ideal for SAP SD interview prep and revision!
