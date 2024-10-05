# Conversion de Message en Représentations Numériques

Ce script Python convertit un message texte en différentes représentations numériques, notamment en valeurs ASCII, hexadécimales, et en bases 16 et 10.

## Description

Le code prend un message en entrée et effectue une série de conversions pour démontrer différentes représentations numériques du même contenu.

## Code source

```python
# Message to be converted
message = "HELLO"

# Step 1: Get the ASCII ordinal values (bytes) of the message
ascii_bytes = [ord(char) for char in message]

# Step 2: Convert the ASCII bytes to hexadecimal
hex_bytes = [hex(byte) for byte in ascii_bytes]

# Step 3: Concatenate the hex bytes into a single hex string
hex_string = ''.join(hex_byte[2:] for hex_byte in hex_bytes)  # Remove '0x' prefix

# Step 4: Convert the concatenated hex string to a base-16 integer
base_16_value = int(hex_string, 16)

# Step 5: Convert the base-16 integer to a base-10 integer
base_10_value = base_16_value

# Print the results
print(f"Message: {message}")
print(f"ASCII Bytes: {ascii_bytes}")
```

## Fonctionnement

1. **Définition du message** :
   - `message = "HELLO"` définit le message à convertir.

2. **Conversion en valeurs ASCII** :
   - `ascii_bytes = [ord(char) for char in message]` convertit chaque caractère en sa valeur ASCII correspondante.

3. **Conversion en hexadécimal** :
   - `hex_bytes = [hex(byte) for byte in ascii_bytes]` convertit chaque valeur ASCII en sa représentation hexadécimale.

4. **Concaténation en une chaîne hexadécimale** :
   - `hex_string = ''.join(hex_byte[2:] for hex_byte in hex_bytes)` concatène les valeurs hexadécimales en une seule chaîne, en retirant le préfixe '0x'.

5. **Conversion en entier base 16** :
   - `base_16_value = int(hex_string, 16)` convertit la chaîne hexadécimale en un entier en base 16.

6. **Conversion en base 10** :
   - `base_10_value = base_16_value` assigne la même valeur à la variable base_10_value, car Python représente déjà les entiers en base 10 par défaut.

7. **Affichage des résultats** :
   - Les résultats sont affichés pour le message original et les valeurs ASCII.
