# binary-tree-traversal--task--python

Set of programming assignments that are designed to test knowledge of traversal methods for binary trees.

### Data structure for representing binary trees

You may assume that for all programming assignments within this problem set the following data class
will be used to represent tree nodes:

```python
class TreeNone:
    def __init__(
        self,
        value: int = 0,
        left: Optional['TreeNone'] = None,
        right: Optional['TreeNone'] = None
    ):
        self.value = value
        self.left = left
        self.right = right
```

For example the following tree could be created using the snippet below:


```mermaid
graph TB

  SubGraph1 --> SubGraph1Flow
  subgraph "SubGraph 1 Flow"
  SubGraph1Flow(SubNode 1)
  SubGraph1Flow -- Choice1 --> DoChoice1
  SubGraph1Flow -- Choice2 --> DoChoice2
  end

  subgraph "Main Graph"
  Node1[Node 1] --> Node2[Node 2]
  Node2 --> SubGraph1[Jump to SubGraph1]
  SubGraph1 --> FinalThing[Final Thing]
end
```


Please use a template for the implementation (`tasks/numbers_and_math.py:get_function_value_in_point`).

Please use a template for the implementation (`tasks/str_operations.py:crack_cipher`).
