# gp_rust

Genetic Programming by rust

## data set

### Terminal Set

The terminal set may consists the following items.

* the program's external inputs. This named variables (e.g `x`, `y`)
* functions with no arguments. For example `rand()`.
* constants. These can be pre-specified, randomly generated as part of the tree creation process, or created by mutation.

### Function Set

In a simple numeric problem, for example, the following functions is Function Set. Basicaly the function set used n GP is typically driven by the nature of the problem domain.

| Kind of primitive | Example(s)    |
|:------------------|--------------:|
| Arithmetic        | +,*,/         |
| Mathmatical       | sin, cos, exp | 
| Boolean           | and, or, not  |
| Conditional       | IF-THEN-ELSE  |
| Looping           | For           |
| etc               | ...           |

### Fitness Function

## References

* [Genetic Programming](http://geneticprogramming.com/)