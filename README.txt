THE SUPPLIER BILL CHECKER — free giveaway from "Build It With AI" (Episode 23)

What you agreed to pay, what actually arrived, what they billed — reconciled line by line:
price drift against your agreed list, quantities billed beyond what was delivered, lines for
goods that never came, the same bill submitted twice under a new number, credits owed to you,
and a dispute note per supplier with every dollar traced.

WHAT'S IN THIS FOLDER
- Supplier_Bill_Checker.html .. THE TOOL — the finished, tested build. One file. Open it in any
                                browser. No internet, no account, nothing you paste leaves your
                                machine, and it never reads the clock — you type the period.
- sample/prices.csv ........... the episode's sample price list (Redbud Auto Repair — fictional,
                                any contact would be @example.com)
- sample/received.csv ......... the episode's sample receiving log
- sample/bills.csv ............ the episode's sample month of supplier bills
- PROMPTS.txt ................. the exact three prompts from the episode, word for word
- checker.py .................. the independent second implementation (Python) used to verify
                                the tool — run: python3 checker.py prices.csv received.csv bills.csv
- engine_v1.js ................ FIRST DRAFT, NOT THE TOOL — kept verbatim, bugs and all (checks
                                bills against themselves, misses the duplicate, flags a credit
                                memo and a price drop as problems)
- engine_v2.js ................ SECOND DRAFT, NOT THE TOOL — kept verbatim (quantity check
                                against the latest delivery slip only, duplicates by invoice
                                number only, floating-point money)

HOW TO USE IT ON YOUR OWN BILLS
1. Open Supplier_Bill_Checker.html. Click "Load the sample shop" to see it work.
2. Make your price list a CSV with columns: Supplier, Item Code, Description, Unit, Agreed Price.
3. Make your receiving log a CSV with columns: Date, Supplier, Item Code, Qty, Reference.
   (No receiving log? Set "receiving log: not kept" — you still get prices and duplicates.)
4. Paste a period's bills as CSV: Invoice, Date, Supplier, Item Code, Description, Qty,
   Unit Price, Line Total.
5. Type the billing period, set your tolerance and duplicate window, and read the refusals
   panel before you trust anything. The tool sends nothing and stores nothing.

If your exports name their columns differently, hand your file and PROMPTS.txt's first prompt
to an AI assistant and tell it what your software calls things.

HONEST LIMITS
- It audits against YOUR price list and YOUR receiving log — if those are wrong, the audit is
  wrong the same way. Keep both honest.
- It has no idea about freight, surcharges, or tax lines; give them item codes and agreed
  prices, or expect them in the check-by-hand list.
- A flagged line is a question for your supplier, not a verdict. Most overcharges are mistakes,
  not malice — the dispute notes are written to be sent politely.
- The sample shop is fictional. Any resemblance is coincidence.

Found a bug? Ask the AI to fix it — and make it prove the fix on the numbers, the way the
episode does, not with reassurance.
