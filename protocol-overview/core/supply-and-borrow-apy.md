# Supply & Borrow APY

## What is APY? <a href="#stable-coin1" id="stable-coin1"></a>

* APY is Initialism of annual percentage yield.
* It intends the total amount of interest over one year.&#x20;
* The annual percentage yield is expressed as an annualized rate.&#x20;
* The adjustment of APY is based on the utilization rate of the asset.

## What is Utilization Rate? <a href="#what-is-utilization-rate" id="what-is-utilization-rate"></a>

_The Utilization Rate is how much of the asset has been utilized_ and is calculated a_s_:

$$
Utilization Rate = Borrowing/(Supplying-Reserves)×100UtilizationRate=Borrowing/(Supplying−Reserves)×100
$$



## **USDT, USDC,APT,ETH**(Single coin1) <a href="#stable-coin1-1" id="stable-coin1-1"></a>

### Borrow APY <a href="#borrow-apy" id="borrow-apy"></a>

* When the utilization rate is **less than 90%** , the annuaized interest rate is calculated as:

$$
Borrow APY= 1.9+ 15 × Utilization RateBorrowAPY=1.9+15×UtilizationRate
$$

* When the utilization rate is **greater than or equal to 90%** , the annualized interest rate is calculated as:

$$
Borrow APY = - 746 + 846 × Utilization RateBorrowAPY=−746+846×UtilizationRate
$$

### Supply APY <a href="#supply-apy" id="supply-apy"></a>

$$
SupplyAPY= Borrow APY×Utilization Rate × 0.85SupplyAPY=BorrowAPY×UtilizationRate×0.85
$$

## Collateral ratio <a href="#collateral-ratio" id="collateral-ratio"></a>



| Asset              | Max Collateral ratio |
| ------------------ | -------------------- |
| USDT               | 80%                  |
| USDC               | 80%                  |
| APT                | 60%                  |
| ETH                | 70%                  |
| BTC                | 70%                  |
| USDT-USDT(LP coin) | 80%                  |
