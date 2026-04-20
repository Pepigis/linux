# 🐧 Linux & Python: Tahák k maturitě

Tento soubor slouží jako rychlá referenční příručka pro praktickou maturitu. Obsahuje základní příkazy, práci se soubory a propojení s Pythonem.

## 📂 1. Navigace a Průzkum
| Příkaz | Popis | Příklad |
| :--- | :--- | :--- |
| `pwd` | Kde právě jsem (cesta) | `pwd` |
| `ls` | Seznam souborů | `ls` |
| `ls -la` | Seznam všech souborů včetně skrytých a detailů | `ls -la` |
| `cd [složka]` | Přesun do složky | `cd Dokumenty` |
| `cd ..` | O úroveň výš | `cd ..` |
| `cd ~` | Návrat do domovské složky | `cd ~` |

---

## 📄 2. Soubory a Složky
| Příkaz | Popis | Příklad |
| :--- | :--- | :--- |
| `mkdir [název]` | Vytvoření složky | `mkdir projekty` |
| `touch [název]` | Vytvoření prázdného souboru | `touch skript.py` |
| `cp [zdroj] [cíl]` | Kopírování | `cp data.txt zaloha.txt` |
| `mv [zdroj] [cíl]` | Přesun nebo **přejmenování** | `mv stary.py novy.py` |
| `rm [soubor]` | Smazání souboru | `rm vypis.txt` |
| `rm -r [složka]` | Smazání složky i s obsahem | `rm -r stara_slozka` |

---

## 📝 3. Práce s obsahem (Čtení a Editace)
- `cat soubor.txt` – Vypíše vše do terminálu.
- `head -n 5 soubor.txt` – Vypíše prvních 5 řádků.
- `tail -n 5 soubor.txt` – Vypíše posledních 5 řádků.
- `grep "chyba" log.txt` – Vyhledá slovo "chyba" v souboru.
- `nano soubor.py` – Jednoduchý editor v terminálu (Uložit: `Ctrl+O`, Zavřít: `Ctrl+X`).

---

## 🐍 4. Linux & Python
### Spuštění skriptu
Máš dvě možnosti, jak spustit Python kód v Linuxu:

1. **Přes interpreter:**
   ```bash
   python3 skript.py
