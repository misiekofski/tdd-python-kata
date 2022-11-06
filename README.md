This is demo repo for Python unit test training

```
└── tests
    ├── __init__.py
    └── test_sum
        ├── __init__.py
        └── test_another_sum.py
```


```bash
pytest
pytest --x # zatrzymaj po pierwszym nieudanym teście
pytest --cov  
pytes --maxfail=2 # zatrzymaj pod dwóch testach które nie przejdą
pytest plik.py # uruchom testy z pliku
pytest folder/ # uruchom testy z folderu
pytest -k "MyClass and not method" # uruchom testy z klasy MyClass których nazwa nie zawiera słowa method
pytest -vvv # bardziej szczegółowy wynik testów
```


