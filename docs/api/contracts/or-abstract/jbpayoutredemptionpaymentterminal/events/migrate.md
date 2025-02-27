# Migrate

Emitted from:

* [`migrate`](/api/contracts/or-abstract/jbpayoutredemptionpaymentterminal/write/migrate.md)

## Definition

```
event Migrate(
  uint256 indexed projectId,
  IJBPaymentTerminal indexed to,
  uint256 amount,
  address caller
);
```

* `projectId` is the ID of the project that was migrated.
* `to` is the terminal that was migrated to.
* `amount` is the total token amount that was migrated.
* `caller` is the address that issued the transaction within which the event was emitted.
