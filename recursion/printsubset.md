## Recursion Tree for Subset Generation

```mermaid
graph TD
    A0["subset([], index=0)"]
    A1["include arr[0] -> subset([1], index=1)"]
    A2["include arr[1] -> subset([1,2], index=2) -> print [1,2]"]
    A3["exclude arr[1] -> subset([1], index=2) -> print [1]"]
    B1["exclude arr[0] -> subset([], index=1)"]
    B2["include arr[1] -> subset([2], index=2) -> print [2]"]
    B3["exclude arr[1] -> subset([], index=2) -> print []"]

    A0 --> A1 --> A2
    A1 --> A3
    A0 --> B1 --> B2
    B1 --> B3
