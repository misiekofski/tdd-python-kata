```python

x = "hello"

# jeżeli warunek zwróci True, nic się nie dzieje:
assert x == "hello"

# jeżeli warunek zwróci False, AssertionError jest rzucone:
assert x == "goodbye"

# nadpisanie treści wyjątku
assert x == "goodbye", "x should be 'hello'"
```


```python
import pytest


def test_zero_division():
    with pytest.raises(ZeroDivisionError):
        1 / 0
```