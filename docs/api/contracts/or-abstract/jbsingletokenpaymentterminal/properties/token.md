# token

Contract: [`JBSingleTokenPaymentTerminal`](/api/contracts/or-abstract/jbsingletokenpaymentterminal/README.md)​‌

Interface: [`IJBSingleTokenPaymentTerminal`](/api/interfaces/ijbsingletokenpaymentterminal.md)

**The token that this terminal accepts.**

# Definition

```
/**
  @notice
  The token that this terminal accepts.
*/
address public immutable override token;
```

* Once set the value cannot be changed.
* The resulting view function can be accessed externally by anyone.
* The resulting function overrides a function definition from the [`IJBSingleTokenPaymentTerminal`](/api/interfaces/ijbsingletokenpaymentterminal.md) interface.
