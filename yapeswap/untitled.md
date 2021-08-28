---
description: >-
  Details the next-generation features of the Yapeswap AMM and provides critical
  details regarding how the AMM functions, pools supported, and fees
---

# Yapeswap AMM

## How is Yapeswap different than the existing AMMs?

Yapeswap is a next generation AMM focused on the smart utilization of liquidity. With a typical AMM, liquidity is only utilized and earning rewards when trades are taking place. In most pools, 80-90% of the liquidity goes unused as only 10-20% is being used for swaps at a given time. In the era of capital efficiency, this is a problem for liquidity providers. 

Yapeswap is providing a solution to this problem by allocating the unused liquidity in our pools to Yearn Finance Vaults \(see glossary\). Yapeswap will automatically adjust the farming ratio, or the balance of liquidity held for trades and the amount that is stored in the yield earning vaults. This rebalancing is based on the overall size of the pool and the demand for liquidity due to trading activity. This description is slightly simplified, but it explains Yapeswap in a nutshell, the AMM that ensures your crypto is working hard to earn you more crypto.

## How it works

How does Yapeswap work in detail? You can simply understand how it works under the hood with the following scenario. 

1. You provide 1M USDC + 1M DAI to the Yape pair.
2. The Yape pair deposits 0.9M USDC & 0.9M DAI to Yearn. \(ex. current avg farming ratio is 90%, min = 85%, max = 95%\)
3. But actual swaps are executed based on the virtual reserves`virtual reserve0 = balance0 + farming0`

   `virtual reserve1 = balance1 + farming1`

   _\*balance refers to the amount remaining in real reserves._

   \*_farming refers to the amount deposited into Yearn vaults._

4. i.e, virtual USDC reserve is 0.1M + 0.9M & virtual DAI reserve is also 0.1M + 0.9M.
5. If someone tries swap function, Yape pair uses the `balance` first, so the gas price almost equals UniV2. But if the `balance` is not enough \(for example, when someone makes a large trade making the farming ratio be outside of min, max\), it withdraws the `farming` asset from Yearn & rebalances the farming ratio.
   * For example, if DAI’s farming ratio is 100% it will be over-farming, so it’ll withdraw 10% from Yearn when rebalance is called.
   * In another case, the USDC farming ratio will be roughly around 80% and it will be under-farming, so it’ll deposit 10% to Yearn at the same time.
6. Anyone can run rebalance function in a permissionless way.
7. When rebalance is called, it takes the net yield and sends it to the fee manager.
8. Fee manager buys back $YAPE using the revenue & distributes them to the $veYAPE holders.

## Pools Supported

The following pools will be supported at V1 launch, with the exception of YAPE/ETH, which will be added to V1 shortly after launch. The development team has chosen these as the first pools to allow the protocol to grow before adding more volatile pairings.

* USDC/ETH
* USDT/ETH
* DAI/ETH
* USDC/USDT
* DAI/USDC
* DAI/USDT
* WBTC/ETH
* WBTC/USDC
* WBTC/USDT
* YAPE/ETH

## Fee Model

1. There is a 0.3% fee for swapping tokens in Yapeswap. 0.25% of the fee goes back to the LP pool and 0.05% of the fee goes to the fee manager for buy-back $YAPE. 
2. All revenues from idle reserves deposited into Yearn vaults go to the fee manager and are also used for buy-back $YAPE. 
3. All $YAPE bought by the fee manager is distributed to $veYAPE holders as dividends. 
4. Liquidity providers can get juicy $YAPE emissions\(~ 60% of total emissions\) instead.
5. Liquidity providers even can get more juicy $YAPE rewards by locking their $YAPE to get $veYAPE

