V shellu (např. v `if` podmínkách) lze testovat různé vlastnosti souborů a čísel.

### Testy typu souboru

| Test | Popis |
| :--- | :--- |
| `-f soubor` | Existuje `soubor` a je to obyčejný soubor? |
| `-d soubor` | Existuje `soubor` a je to adresář? |

### Testy práv k souboru

| Test | Popis |
| :--- | :--- |
| `-r soubor` | Mohu číst `soubor`? |
| `-w soubor` | Mohu zapisovat do `souboru`? |
| `-x soubor` | Mohu `soubor` spustit? |
| `-O soubor` | Vlastním `soubor`? |

| Test | Popis |
| :--- | :--- |
| `cislo1 -eq cislo2` | Čísla 1 a 2 se rovnají (equal) |
| `cislo1 -ne cislo2` | Čísla se nerovnají (not equal) |
| `cislo1 -lt cislo2` | Číslo 1 je menší než číslo 2 (less than) |
| `cislo1 -le cislo2` | Číslo 1 je menší nebo rovno (less or equal) |
| `cislo1 -gt cislo2` | Číslo 1 je větší než číslo 2 (greater than) |
| `cislo1 -ge cislo2` | Číslo 1 je větší nebo rovno (greater or equal) |

### 2. Logické výrazy (Úvod a tabulky)


## Příklad `if-then-else`

Základní struktura pro větvení skriptu.


# Příklad: Ověření, zda uživatel 'roman' existuje v systému
if grep -q roman /etc/passwd; then
  echo "roman je tam"
else
  echo "neni tam"
fi

### 4. Tvrdý odkaz (Hard Link)


## Tvrdý odkaz (Hard Link)

V základním unixovém systému souborů jsou všechny soubory a adresáře popsány v tabulce **i-uzlů** (i-node). Každý i-uzel má své číslo, které je pořadovým číslem položky v tabulce i-uzlů. Tato tabulka je umístěna na začátku systému souborů a má pevnou velikost stanovenou při jeho vytváření.

V každém adresáři jsou uloženy dvojice údajů:
1.  Jméno položky (souboru nebo podadresáře)
2.  Číslo i-uzlu

Všechny ostatní údaje o souboru (vlastník, práva, velikost, časové značky atd., vyjma obsahu) jsou uloženy v i-uzlu.

Díky této konstrukci může na jeden soubor (tj. na jeden i-uzel) ukazovat více jmen ze stejného adresáře nebo z různých adresářů.

Číslo i-uzlu uvedené v adresáři je tzv. **tvrdým odkazem** na soubor. Ukazuje-li na soubor více jmen, pak má soubor více tvrdých odkazů. Aktuální počet tvrdých odkazů na soubor je uveden v i-uzlu.

Smazáním jména souboru v adresáři (např. příkazem `rm`) snížíte počet tvrdých odkazů o jedničku. Jakmile počet tvrdých odkazů dosáhne nulové hodnoty, systém položku i-uzlu smaže a uvolní datové bloky (obsah souboru).
