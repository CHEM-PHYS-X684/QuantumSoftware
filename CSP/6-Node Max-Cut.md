### 6-Node example
Consider the following graph of 6 nodes. We want to partition this into two groups, a `Top` and a `Bottom`:
```mermaid 
flowchart LR
    1(1) 
    2(2)
    3(3)
    4(4)
    5(5)
    6(6)
    1 --- 2
    2 --- 3
    3 --- 4
    4 --- 5
    5 --- 6
    3 --- 5
    1 --- 3
    1 --- 6
    4 --- 6
```

The following cut breaks 7 edges:
```mermaid
flowchart LR
    subgraph Top
	    1 
	    2
	    4
	    5
	end
    subgraph Bottom
	    3
	    6
	end
    1 --- 2
    2 --- 3
    3 --- 4
    4 --- 5
    5 --- 6
    3 --- 5
    1 --- 3
    1 --- 6
    4 --- 6
```

However, this is not unique, we could have also achieved an equally good cut by just adding node `2` to `R`:
```mermaid
flowchart LR 
    subgraph Top 
	    1 
	    4
	    5
	end
    subgraph Bottom
	    2
	    3
	    6
	end
    1 --- 2
    2 --- 3
    3 --- 4
    4 --- 5
    5 --- 6
    3 --- 5
    1 --- 3
    1 --- 6
    4 --- 6
```

As such, there are generally multiple solutions that are equally good. In a quantum mechanical context, we refer to this as [degeneracy](https://en.wikipedia.org/wiki/Degenerate_energy_levels).

[Up](./README.md)