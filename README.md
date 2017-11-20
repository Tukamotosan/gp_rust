# gp_rust

Genetic Programming by rust

## data set

### Step 1: Terminal Set

The terminal set may consists the following items.

* the program's external inputs. This named variables (e.g `x`, `y`)
* functions with no arguments. For example `rand()`.
* constants. These can be pre-specified, randomly generated as part of the tree creation process, or created by mutation.

### Step 2: Function Set

In a simple numeric problem, for example, the following functions is Function Set. Basicaly the function set used n GP is typically driven by the nature of the problem domain.

| Kind of primitive | Example(s)    |
|:------------------|--------------:|
| Arithmetic        | +,*,/         |
| Mathmatical       | sin, cos, exp | 
| Boolean           | and, or, not  |
| Conditional       | IF-THEN-ELSE  |
| Looping           | For           |
| etc               | ...           |

### Step 3: Fitness Function

The sample code of evaluate function is the following code.
Basicaly, fitness function evalueates all possible test data(`x1,x2,xN`).

```python
def eval(expr):
    # expr is an expression in prefix notation
    if expr is list:
        # expr[0] represents the primitive at
        # the root of the expression
        proc = expr[0]
        if proc is function:
            # evalueate function
            value = proc(expr[1], expr[2], ...)
        else:
            value = proc(expr[1], expr[2], ...)

    else:
        if expr is variable or expr is constant:
            # just read the value
            value = expr()
        else
            # constant
            value = expr()
    return value
```

### Step 4: GP Parameters

The control parameters are the following items.

* `population size`
* `probabilities of performing the genetic operations`
* the number of runs `R`
* the number of generations `G`
* the size of the populations `P`
* average size of the programs `s`
* the number of fitness cases `F`

### Step 5: Termination and solution designation

$$c^2=a^2 + b^2 $$

These parameters are depend too much on the details of the application.


## References

* [Genetic Programming](http://geneticprogramming.com/)
