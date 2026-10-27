---
description: Connect Claude to your RobynFood restaurant (Google sign-in at table.robynfood.com)
---

Connect the RobynFood connector for the user.

1. Call the `restaurant_overview` tool of the RobynFood connector. If the connector is not connected yet, Claude opens the sign-in: the user continues with Google at table.robynfood.com.
2. Explain the steps the user will see in the browser, in one short list:
   - Continue with Google.
   - Create the restaurant website (only the first time).
   - AI Assistant add-on: book it if it is not booked yet, then press "Connect Claude".
3. When the tool answers, confirm the restaurant name and say what can be asked now (reservations, tables).
4. If the answer says the AI add-on is not active, tell the user to open table.robynfood.com > Claude (AI). Do nothing else.
