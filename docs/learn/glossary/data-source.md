# Data source

#### What everyone needs to know

* A data source contract is a way of providing extensions to a treasury that either override or augment the default [`JBPayoutRedemptionPaymentTerminal`](/api/contracts/or-abstract/jbpayoutredemptionpaymentterminal/README.md) functionality.
* A data source contract can be used to provide custom data to the [`JBPayoutRedemptionPaymentTerminal.pay(...)`](/api/contracts/or-abstract/jbpayoutredemptionpaymentterminal/write/pay.md) transaction and/or the [`JBPayoutRedemptionPaymentTerminal.redeemTokensOf(...)`](/api/contracts/or-abstract/jbpayoutredemptionpaymentterminal/write/redeemtokensof.md) transaction.
* A data source is passed contextual information from the transactions, from which it can derive custom data for the protocol to use to affect subsequent behaviors in the pay and redeem transactions. Contextual information from the pay transaction is passed to the data source in the form of [`JBPayParamsData`](/api/data-structures/jbpayparamsdata.md) , and contextual information from the redeem transaction is passed to the data source in the form of [`JBRedeemParamsData`](/api/data-structures/jbredeemparamsdata.md).
* A data source is responsible for specifying any [delegate](delegate.md) hooks that should be triggered after the core functionality of a [`pay(...)`](/api/contracts/or-abstract/jbpayoutredemptionpaymentterminal/write/pay.md) or [`redeemTokensOf(...)`](/api/contracts/or-abstract/jbpayoutredemptionpaymentterminal/write/redeemtokensof.md) transaction executes successfully.
* Each [`IJBPaymentTerminal`](/api/interfaces/ijbpaymentterminal.md) fork can leverage data sources in unique ways.

#### What you'll want to know if you're building

* A data source must adhere to the [`IJBFundingCycleDataSource`](/api/interfaces/ijbfundingcycledatasource.md) interface.
* A data source contract can be specified in a funding cycle, along with flags that indicate if the funding cycle should `useDataSourceForPay` and/or `useDataSourceForRedeem`. These are set either in [`JBController.launchProjectFor(...)`](/api/contracts/or-controllers/jbcontroller/write/launchprojectfor.md) or [`JBController.reconfigureFundingCyclesOf(...)`](/api/contracts/or-controllers/jbcontroller/write/reconfigurefundingcyclesof.md).
* A funding cycle's data source is called upon in [`JBSingleTokenPaymentTerminalStore.recordPaymentFrom(...)`](/api/contracts/jbsingletokenpaymentterminalstore/write/recordpaymentfrom.md) and in [`JBSingleTokenPaymentTerminalStore.recordRedemptionFor(...)`](/api/contracts/jbsingletokenpaymentterminalstore/write/recordredemptionfor.md).
* If a data source is not specified in a funding cycle, or if flags aren't explicitly set, default protocol data will be used.

[Get started building data sources](/build/treasury-extensions/data-source.md).
