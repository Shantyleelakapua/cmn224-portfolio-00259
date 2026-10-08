# Week 9 — Behavioural Diagrams (Lab 6)

## AI Disclosure

I used an AI assistant to generate initial PlantUML syntax drafts for all four diagrams. I did not use it to decide the content — the actors, use cases, classes, states, and business rules were all taken from my SRS (Task 2) and my Week 5 deployment diagram.

Specifically, I:
- Chose the four actors (Depot Clerk, Treasurer, Committee Member, Member) from the SRS roles
- Selected the PaymentBatch lifecycle for the state diagram because the two-person approval rule is the core business constraint
- Built the offline/USB-sync branch in the activity diagram to match the deployment constraint that the depot has no mains power or fixed internet
- Verified every class attribute against the SRS in-scope list (membership number, village, phone, produce type, weight, grade, price per kg, slip number)
- Confirmed the multiplicity on PaymentBatch → PaymentSlip (1..*) reflects the rule that a batch cannot be approved if it contains no slips
- Rendered and visually checked each diagram before committing

The AI draft initially missed the USB-sync path and the committee co-sign step. I added both after cross-referencing the SRS.

## Files

| File | Diagram |
|------|---------|
| usecase.puml / usecase.png | Part A — Use case diagram |
| class.puml / class.png | Part B — Class diagram |
| state.puml / state.png | Part C — State diagram (PaymentBatch) |
| activity.puml / activity.png | Part D — Activity diagram (intake workflow) |   