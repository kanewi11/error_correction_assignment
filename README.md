
## 1.
```
def to_camel_case(text: str) -> str:
   return re.split('_|-', text)[1] + ''.join(word.title() for word in re.split('_|-', text)[1::])
```
## 2.
```
class SingletonMeta(type):

    _instances = {}
    
    def __call__(cls, *args, **kwargs):
        if cls not in cls._instances:
            cls._instances[cls] = super(Singleton, cls).__call__(*args, **kwargs)
        return cls._instances[cls]
```
## 3.
```
count_bits = lambda n: bin(n).count('1')
```
## 4.
```
def digital_root(n: int) -> int:
    return n if n < 10 else digital_root(sum(map(int, str(n))))
```
## 5.
```
even_or_odd = lambda number: 'Even' if number % 2 == 0 else 'Odd'
```