# IJBFundingCycleBallot

```
interface IJBFundingCycleBallot {
  function duration() external view returns (uint256);

  function stateOf(
    uint256 _projectId,
    uint256 _configuration,
    uint256 _start
  ) external view returns (JBBallotState);
}
```
