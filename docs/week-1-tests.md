# Week 1: the 12 tests

1. New transaction starts Open with a zero total
2. Adding lines updates the total
3. Cannot add a line once tendering has started
4. Cannot complete when tenders are short of the total
5. Completes when tenders exactly cover the total
6. Cash over the total completes and records the change
7. Card tender above the amount owed is rejected
8. Split tender (card plus cash) completes correctly
9. Open transaction can be voided
10. Completed transaction cannot be voided
11. A card tender with no reply stays Pending and blocks completion
12. A declined card tender does not count towards the total paid

Done when: all 12 pass locally and on GitHub Actions, committed with clear messages.
