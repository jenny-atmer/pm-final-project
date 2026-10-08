# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** Pay-after-you-decide invoice (Major Project): the only thing that makes this more than a Riverty-branded debit card, and it spans later sprints.
- **My finalized Must-Haves (after overriding the AI):** A card purchase at any Mastercard-accepting merchant creates a Riverty invoice instead of debiting her account. This is the moment of misery. Start online-only, as the 2023 risk Q&A proposed.
Authorisation against a single issuer-set limit. Without it there is no card. There are no user-set limits.
One invoice per purchase, showing amount and due date in the app. Single invoices were the preferred model in the 2023 research.
No money leaves her account before the due date unless she chooses. Any automatic debit is off by default or requires her explicit consent. This is the "when" half of the goal.
Pay-now option on any open invoice. She can pay early whenever she decides to keep the item.
A due date long enough to receive and decide. Card purchases lack order and shipment data (2023 risk Q&A), so the due date is a fixed-length proxy. The length must be set with Legal and Risk. Germany's online withdrawal period is 14 days from receipt of goods (verify with Legal), so a 14-day due date counted from purchase can expire before she has decided.
Reporting a return pauses the due date on that invoice. Klarna does this and interviewees praised it. It is now a must-have because it is the closest sprint-1 approximation of "after you decide".
A confirmed refund reduces or cancels the invoice, visibly to her. The process can be ops-assisted in sprint 1, but it must exist, or "only pay for what I keep" is false.
- **What I demoted from Must → Should/Won’t, and why:** Pay-now option on any open invoice. She can pay early whenever she decides to keep the item.

One invoice per purchase, showing amount and due date in the app. Single invoices were the preferred model in the 2023 research.

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** a lot of clear user stories and requirements

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** A purchase marked as Returned just disappeared from the list (should be  marked "Paused until the refund is confirmed")
- **My prototype, as a link or a screenshot (publish or share from your tool; in Lovable that is Share → Share Preview, in Bolt Publish → Web. No share URL? Screenshot the working flow):** https://claude.ai/artifact/YTrFkJUgWZ2giBovrhRCn8?sk=QyEwEByImghNJ8ejMzMrZQ
