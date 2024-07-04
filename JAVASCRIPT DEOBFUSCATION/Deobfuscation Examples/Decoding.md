# Codificação

## Base64
```
echo -n "https://www.exemplo.eu/" | base64
Resultado: aHR0cHM6Ly93d3cuZXhlbXBsby5ldS8=

```

## Decodificação:
```
echo "aHR0cHM6Ly93d3cuZXhlbXBsby5ldS8=" | base64 -d
```
Resultado: https://www.exemplo.eu/

## Hexadecimal (Hex)
Codificação:
```
echo -n "https://www.exemplo.eu/" | xxd -p
```
Resultado: 68747470733a2f2f7777772e6578656d706c6f2e65752f

## Decodificação:
```
echo "68747470733a2f2f7777772e6578656d706c6f2e65752f" | xxd -p -r
```
Resultado: https://www.exemplo.eu/

## Rot13
Codificação:

```
echo "https://www.exemplo.eu/" | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
Resultado: uggcf://jjj.rkrzcyb.rh/

## Decodificação:
```
echo "uggcf://jjj.rkrzcyb.rh/" | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
Resultado: https://www.exemplo.eu/

Esses comandos são úteis para manipular e entender textos codificados usando essas técnicas comuns de criptografia e obfuscação.
