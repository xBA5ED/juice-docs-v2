# metadataContentOf

Contract: [`JBProjects`](/api/contracts/jbprojects/README.md)

Interface: [`IJBProjects`](/api/interfaces/ijbprojects.md)

**The metadata for each project, which can be used across several domains.**

# Definition

```
/** 
  @notice 
  The metadata for each project, which can be used across several domains.

  _projectId The ID of the project to which the metadata belongs.
  _domain The domain within which the metadata applies. Applications can use the domain namespace as they wish.
*/
mapping(uint256 => mapping(uint256 => string)) public override metadataContentOf;
```

* Arguments:
  * `_projectId` is the ID of the project to which the metadata belongs.
  * `_domain` is the domain within which the metadata applies.
* The resulting view function can be accessed externally by anyone.
* The resulting function overrides a function definition from the [`IJBProjects`](/api/interfaces/ijbprojects.md) interface.
