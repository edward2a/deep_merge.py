# Deep Dict Merge

dmerge - Recursively merge two dictionaries

### Installation

pip install dmerge

### Usage

```python
from dmerge import deep_merge

a = {'a': 33,
     'b': {'x': 'z',
           'y': { 'asdf': 'fdsa'}
          }
    }
b = {'x': 44,
     'm': ['2', 'dd', 'asdf'],
     'b': {'y': {'fdsa': 'asdf'}},
           '33': {'rewq': 'qwer'}
    }

r = deep_merge(a,b)
```

The result will be:
```python
{'b': {'x': 'z',
       'y': {'asdf': 'fdsa',
             'fdsa': 'asdf'
            }
      },
 'x': 44,
 'm': ['2', 'dd', 'asdf'],
 '33': {'rewq': 'qwer'},
 'a': 33
}
```
