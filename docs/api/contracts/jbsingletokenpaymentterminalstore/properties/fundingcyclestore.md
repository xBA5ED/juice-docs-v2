# fundingCycleStore

Contract: [`JBSingleTokenPaymentTerminalStore`](/api/contracts/jbsingletokenpaymentterminalstore/README.md)​‌

Interface: [`IJBSingleTokenPaymentTerminalStore`](/api/interfaces/ijbsingletokenpaymentterminalstore.md)

**The contract storing all funding cycle configurations.**

# Definition

```
/** 
  @notice 
  The contract storing all funding cycle configurations.
*/
IJBFundingCycleStore public immutable override fundingCycleStore;
```

* Once set the value cannot be changed.
* The resulting view function can be accessed externally by anyone.
* The resulting function overrides a function definition from the [`JBSingleTokenPaymentTerminalStore`](/api/interfaces/ijbsingletokenpaymentterminalstore.md) interface.
