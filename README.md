# Bitcoin Address
Bitcoin Wallet Address Generator

This is a simple Bitcoin wallet address generator coded in Python 3.
It generates a Private Key in different formats (hex, wif and compressed wif) and corresponding Public Addresses, raw, P2WPKH addresses starting with prefix 1, P2SH addresses starting with prefix 3 as part of Segwit soft fork and Bech32 addresses with prefix bc1 P2WPKH and P2WSH.

## Installation
```
pip install bitcoinaddress
```

## Usage
###### Example 1
```
from bitcoinaddress import Wallet

wallet = Wallet()
print(wallet)
```

###### Output:
```
Private Key HEX: 562997b9379008a97d7e4cbf6f19c41d4c348de96199aba44c79e3b32f1cc174
Private Key WIF: 5JUEV9pjH4o16NRTBsaN18ehDNaqSsD66EySbT1BZsSvYQttmga
Private Key WIF compressed: Kz7CXFwfbuk3QhYvazEFhamNVcGLqAcMU8g7y3moe5fRKZXZaj7k

Public Key: 04e7ba7ecb0fccaae6bbe1d1493a1dc2e6d266006374411af3ff82546490ffef67cd2e06d0e385b695fe2eaf436d61559837571d989b413e75d763127f628a05f3
Public Key compressed: 03e7ba7ecb0fccaae6bbe1d1493a1dc2e6d266006374411af3ff82546490ffef67

Public Address 1: 1oKgBdYNyNiW5ntjEpJwsJwRZ1Qr9cPce
Public Address 3: 3K55C3EdCJYZWoc95Tt7CbXnUkDSaVeZrC
Public Address bc1 (P2WPKH): bc1q363sj8rhw0uqmxurraa0rtydhp32cyuke4lfwt 
Public Address bc1 (P2WSH): bc1qsy38c4na9fm0y5pvyhja0hscpx5my290pgwgeq5eduvdqmejkwyq0whxpw
```

###### Example 2
```
from bitcoinaddress import Address, Key

key = Key()
key_dict = key.generate()
print(key_dict)

address = Address(key)
address_dict = address.generate()
print(address_dict)
```

###### Output:
```
{'hex': '060e9a032e49db4eb758d60d96c14fea64e410d87ac826cc3c133047528935f6', 
'wif': '5HrxJNp4LHGtkWDZWPjbr3JQvAamdFxQkDAksjrWFy8QG8EWsHJ', 
'wifc': 'KwRV5hGhi6q9R1xSUjM2oT9rZfJ3y31Zoii4ex9W94jffRrD8t4G'}

{'pubkey': '04f9f7a04a482885ad3348d1a02e928ca659fb2a40ece79223329fc44ef518c810f026be9f40149f31a3fb077c3b18019cd5bb837b3d923627ec5e396ed63d3ce7', 
'pubkeyc': '03f9f7a04a482885ad3348d1a02e928ca659fb2a40ece79223329fc44ef518c810', 
'pubaddr1': '1Hyvgn8wwVab4d2qCXMKr1dJZRXktbRPXo', 
'pubaddr3': '3KG5NRa5GwWVqoQGvL3KC4zPqo8W33ikQT', 
'pubaddrbc1_p2wsh': 'bc1qad8wsh8evtz5wjueyh2hy4zgt5c0ahwtl4pq793058wrercagwwqyx5mzt', 
'pubaddrbc1_p2wpkh': 'bc1q270rv5ezzuepa0pyr0wujuuwr2qtegwgfrt78t'}
```


## Authors
Pedro Fortes and others who contribute.

## License
This software is distributed under the terms of the MIT License. 
See the file 'LICENSE' in the root directory of the present distribution, or http://opensource.org/licenses/MIT.
