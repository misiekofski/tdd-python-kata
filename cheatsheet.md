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


```python
import pytest


def myfunc():
    raise ValueError("Exception 123 raised")


def test_match():
    with pytest.raises(ValueError, match=r".* 123 .*"):
        myfunc()
```


```python
from myfuncs import div
import pytest

TEST_DIV_DATA = (
    (0, 9, 0),
    (8, 4, 2),
    (99, 3, 33)
)

@pytest.mark.parametrize("a, b, result", TEST_DIV_DATA)
def test_div(a, b, result):
    assert div(a, b) == result
```

```python
@pytest.mark.skip(reason="komunikat")
def test_method_1():
    pass
```

```python
@pytest.mark.skipif(mylib.__version__ < (2, 0), reason="Nie wykonuje się w wersji < 2.0")
def test_method_2():
    pass
```