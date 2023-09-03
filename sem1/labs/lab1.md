# Лабораторная работа №1

Напишите сканер портов на любом языке программирования. Сканер должен быть способен:
- Сканировать порты у указанного ip-адреса или домена (вводится в консоли)
- Порты должны перебираться в указанном диапазоне (вводится в консоли)
- Если порт открыт, то необходимо вывести информацию об этом в консоль

Пример сканера на Python без специальных условий:

```python
import socket

ip = 'vvsu.ru'
port = 7777

try:
    connection = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    connection.settimeout(1)
    result = connection.connect_ex((ip, port))
    if result:
      print(f'Port {port} is open')
except Exception as e:
    pass
```
