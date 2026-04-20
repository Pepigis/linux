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
| `cp -r [zdroj] [cíl]` | Kopírování celé složky | `cp -r slozka1/ slozka2/` |
| `mv [zdroj] [cíl]` | Přesun nebo **přejmenování** | `mv stary.py novy.py` |
| `rm [soubor]` | Smazání souboru | `rm vypis.txt` |
| `rm -r [složka]` | Smazání složky i s obsahem | `rm -r stara_slozka` |

---

## 📝 3. Práce s obsahem (Čtení a Editace)
- `cat soubor.txt` – Vypíše vše do terminálu.
- `less soubor.txt` – Otevře text pro čtení (ukončíš klávesou `q`).
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
   ```

2. **Jako spustitelný soubor:**
   - Na první řádek skriptu přidej "Shebang": `#!/usr/bin/env python3`
   - Nastav souboru práva ke spuštění: `chmod +x skript.py`
   - Spusť přímo: `./skript.py`

### Instalace knihoven
```bash
pip install requests
```

---

## 🛡️ 5. Práva a Systém
### chmod (Change Mode)
Nastavení práv pomocí čísel (čtení=4, zápis=2, spuštění=1):
- `chmod 755 skript.py` – Vlastník může vše (7), ostatní jen číst a spouštět (5 a 5).
- `chmod 644 data.txt` – Vlastník může číst/psát (6), ostatní jen číst (4 a 4).
- `chmod +x skript.py` – Rychlé přidání práva ke spuštění.

### Systémové nástroje a procesy
- `sudo [příkaz]` – Spuštění příkazu s administrátorskými právy (root).
- `top` / `htop` – Přehled procesů (procesor, RAM) v reálném čase.
- `ps aux` – Seznam všech běžících procesů.
- `kill [PID]` – Ukončení procesu podle jeho ID.
- `df -h` – Kolik zbývá místa na disku.

---

## 🚀 6. Tipy a Triky (Záchranné kruhy)
- **TAB (Tabulátor):** Doplňování názvů souborů a příkazů.
- **Šipka nahoru:** Vrací k předchozím příkazům.
- **Ctrl + C:** Násilné ukončení zaseknutého programu nebo skriptu.
- **clear:** Vyčištění obrazovky terminálu.
- **man [příkaz]:** Manuál k jakémukoliv příkazu (např. `man ls`). Zavírá se klávesou `q`.
