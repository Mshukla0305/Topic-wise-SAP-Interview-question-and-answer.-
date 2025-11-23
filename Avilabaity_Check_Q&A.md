# SAP SD – Availability Check  
## Interview Questions & Answers (Beginner to Advanced)

This file contains the most commonly asked **SAP SD Availability Check** interview questions along with simple, clear answers.

---

## ❓ 1. What is Availability Check in SAP SD?
**✔ Answer:**  
Availability Check is a process in SAP where the system checks if enough stock is available in the plant to confirm a customer’s order. It tells how much quantity is available and on which date delivery is possible.

---

## ❓ 2. At which level does SAP perform Availability Check?
**✔ Answer:**  
Availability Check happens at **Plant level**.  
For every sales order item, SAP checks stock only in the assigned plant.

---

## ❓ 3. How does SAP determine the Plant in a Sales Order?
**✔ Answer:**  
SAP uses this priority sequence:
1. Customer–Material Info Record  
2. Ship-to Party Master  
3. Material Master  
(You can also enter the plant manually.)

---

## ❓ 4. What is Material Availability Date?
**✔ Answer:**  
It is the date on which material must be available in stock so that delivery can happen on time.  
SAP calculates this using **backward or forward scheduling** (transportation time + loading time + picking time).

---

## ❓ 5. What controls the type of Availability Check for a material?
**✔ Answer:**  
In **Material Master → Sales: General/Plant**, there is a field called **Availability Check**.  
This field tells SAP *which stock types, orders, and rules* should be used for checking.

---

## ❓ 6. What stock elements are considered in Availability Check?
**✔ Answer:**  
Depending on customizing, SAP can include:
- Safety Stock  
- Unrestricted Stock  
- Stock in Transfer  
- Stock in Quality Inspection  
- Purchase Orders  
- Production Orders  
- Sales Orders  
- Reservations  

---

## ❓ 7. What is the difference between ATP Check and Availability Check?
**✔ Answer:**  
ATP = Available to Promise  
Availability Check = Complete stock checking logic  

In SD:
- ATP is the **result**  
- Availability Check is the **process**  

ATP quantity = Stock − All confirmed requirements.

---

## ❓ 8. What is Transfer of Requirements (TOR)?
**✔ Answer:**  
When a sales order is created, SAP sends the required quantity to **MRP** so that planning or procurement can happen.  
TOR ensures future availability.

---

## ❓ 9. What is the difference between Complete Delivery and Partial Delivery?
**✔ Answer:**  
- **Complete Delivery** → Customer wants full quantity in one delivery.  
- **Partial Delivery** → Customer accepts delivery in multiple parts if full stock is not available.  

This setting is controlled in:
- Customer Master  
- Customer–Material Info Record  
- Sales Order  

---

## ❓ 10. Where do we customize Availability Check settings?
**✔ Answer:**  
Path:  
`IMG → SD → Basic Functions → Availability Check and Transfer of Requirements`

Here we define:
- Checking Group  
- Checking Rule  
- Scope of Check  
- Stock determination rules  

---

## ❓ 11. What is Checking Group?
**✔ Answer:**  
Checking Group controls:
- Whether requirements should be transferred to MRP  
- Whether individual or collective requirements are created  
- Which types of stock are considered  

Checking group is assigned in the **Material Master**.

---

## ❓ 12. What is Checking Rule?
**✔ Answer:**  
Checking Rule defines **how** SAP should check availability during different SD transactions:
- Sales Order  
- Delivery  
- Backorder Processing  

Checking Rule + Checking Group = Scope of Check.

---

## ❓ 13. What is Scope of Check?
**✔ Answer:**  
Scope of Check tells SAP:
- What stock types to consider  
- Which receipts & issues to include  
- Whether to include safety stock  
- Whether to include reservations  

---

## ❓ 14. What is Backorder Processing?
**✔ Answer:**  
When some orders cannot be confirmed due to insufficient stock, SAP allows you to re-check and re-confirm quantities. This is called **Backorder Processing**.

---

## ❓ 15. Can Availability Check be deactivated?
**✔ Answer:**  
Yes.  
In Material Master, if you set Checking Group = **00 (No Check)**, SAP will not perform availability check for that material.

---

## ❓ 16. What is Replenishment Lead Time (RLT)?
**✔ Answer:**  
RLT is the total time needed to refill stock (procurement or production time).  
If no stock exists, SAP uses RLT to propose a delivery date.

---

## ❓ 17. Name the types of Availability Checks used in SAP.
**✔ Answer:**  
Common checks are:
- Check against ATP  
- Check against planning  
- Check against replenishment  
- Gamma check (rare in SD)  

---

## ❓ 18. How does ATP help the sales order?
**✔ Answer:**  
ATP tells SAP:
- How much quantity can be committed  
- On which earliest date  
- Whether partial confirmation is required  

---

## ❓ 19. What happens if stock is not available?
**✔ Answer:**  
SAP can:
1. Propose a later delivery date  
2. Confirm partial quantity  
3. Reject schedule line  
4. Send TOR to MRP for future planning  

---

## ❓ 20. Explain the most common interview confusion:  
### “Is availability check done at header or item level?”
**✔ Answer:**  
Availability Check is always performed **at item level**, because each item may have a different plant, schedule, material, and delivery rule.

---

## ⭐ Conclusion

This file contains the **top 20 interview questions** that almost all recruiters ask for SAP SD Availability Check.  
All answers are written in **clean, simple, interview-ready language**.

