---
description: >-
  The loan interest rate calculation uses the kink point interest rate model
  (each type of Token is a market, and the interest rates between the markets do
  not interfere with each other)
cover: ../../.gitbook/assets/761663813436_.pic.jpg
coverY: 0
---

# Interest Rate Model

* When the capital utilization rate of the current market is less than kink points (kink point is 80% by default)
* Use linear interest rate growth model, interest rate grows slowly
* When the capital utilization rate in the market is greater than the kink point, interest rate growth will suddenly accelerate
* interest rate is increasing non-linearly
* The calculation formula for borrowing interest rate is as follows:

```
util = Borrow / (Cash + Borrow)
    if util <= kink {
        borrow_rate = util * multiplier_per_block  + base_rate_per_block;
    } else {
        normal_rate = kink * multiplier_per_block  + base_rate_per_block;
        excess_util = util - kink;
        borrow_rate = excess_util * jump_multiplier_per_block + normal_rate;
    }
```
