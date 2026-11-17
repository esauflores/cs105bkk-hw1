# HW1 notes

## What did you try?

I started with `MenuItem` (the `price` setter, `__repr__` and `__eq__`), then `PromoItem.cost`, `Order` and `cheapest`. I ran `python -m pytest` after each part, and also tried the edge cases from the README by hand: a price of 0, an empty order, food of exactly 300 baht, and a tie in `cheapest`.

## What broke, and how did you fix it?

Creating my repository with "Use this template" didn't work well for the Actions check, so I made an empty `cs105bkk-hw1` repository and pushed my clone to it with `git push -u origin main`. In the code, the trap was `Order.__init__`: storing `lines` directly would share the caller's list, so I store `list(lines)`, which makes a new copy every time.

## What would you do differently next time?

Next time I would write the edge-case checks as my own pytest tests instead of trying them by hand, because then they run on every push like the given tests.
