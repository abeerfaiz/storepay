# Domain rules

- **Money**: a record holding an amount in pence (`long`) and a currency. Never `double`.
- **Transaction**: belongs to a store and a till. States: Open → Tendering → Completed, or Open → Voided.
- Lines can only be added while the transaction is Open. The total is the sum of the lines.
- **Tenders** are Cash, Card or GiftCard, each with an amount and a status (Pending, Approved, Declined).
- Only **Approved** tenders count towards the total paid.
- A **Pending** card tender blocks completion until its outcome is known (the "no reply" screen).
- A transaction completes only when approved tenders cover the total.
- **Change can only come from cash.** A card tender cannot exceed what is still owed.
- A completed transaction cannot be voided. Refunds come later as their own transaction.
