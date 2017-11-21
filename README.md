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

These parameters are depend too much on the details of the application.

## Chapter 5 Alternative Initialisations and Operators in Tree-based GP

### 5.2.2 Mutation Cookbook

#### Subtree mutation

This mutation replace a randomly selected subtree with anothe rrandomly created subtree(Koza, 1992, page 106).

#### Size-fair subtree mutation

This mutation was proposed in two forms by Langdon(1998). The new random subtree is, on average, the same size as the code it replaces. The size of the random code is given either by the size of another random subtree in the program or chosen at random in the range `[l/2, 3l/2]` (where `l` is the size of the subtree being replaced). 

#### Node replacement mutation(point mutation)

This mutation is similar to bit string mutation(like GA's mutation) in htat it randomly changes a point in the individual.

#### Mutating constants systematically

### 5.3 GP Crossover

* one-point crossover(Langdon and Poli, 2002; Poli and Langdon, 1997, 1998a)
* Unifrom crossover
    * likes GA
* context-preserving crossover(D'haeseller, 1994)
* size-fair crossover (Langdon, 1999a, 200)

## Chapter 6 Modules, Grammatical and Developmental Tree-based GP

### 6.1 Evolving Modular and Hierarchical Structures

#### 6.1.1 Automatically Defined Functions



## References

* [Genetic Programming](http://geneticprogramming.com/)
