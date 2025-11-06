# Zápisky a příkazy z Unixu

## Sada příkazů (Příklad workflow)

Následující příkazy ukazují typickou práci se soubory a adresáři, včetně přesměrování a oprávnění.

```bash
# Přepnutí do kořenového adresáře
cd /

# Vytvoření adresáře STUDENT (vyžaduje sudo)
sudo mkdir STUDENT
cd /STUDENT

# Vytvoření prázdných souborů
sudo touch co1 co2 co3

# Otevření souboru co1 v editoru nano (vyžaduje sudo)
sudo nano co1

# Nastavení plných práv (čtení, zápis, spuštění) pro všechny
# na adresář /STUDENT a vše v něm (rekurzivně)
sudo chmod -R 777 /STUDENT

# Přidání textu "jedna a jedna" na konec souboru co1
echo "jedna a jedna" >> co1

# Zobrazení posledních 2 řádků souboru co1
tail -2 co1

# Znovu se "dotkneme" souborů (aktualizuje čas poslední změny)
sudo touch co1 co2 co3

# Zkopírování souboru co2 na Plochu
sudo cp co2 ~/Plocha

# Uložení výpisu 'ls -l' do souboru zk3 na Ploše
ls -l > ~/Plocha/zk3

# Přepnutí na Plochu
cd ~/Plocha

# Přidání textu na konec souboru zk3
echo "s maturitou je to snadne" >> zk3

# Vypsání obsahu zk3
cat zk3

# Vypsání zk3 a zároveň uložení výstupu do souboru 'ok'
cat zk3 | tee ok

# Z souboru 'ok' vyhledání řádků obsahujících 'o2'
# a uložení výsledku do 'filtr1' (a zároveň vypsání)
cat ok | grep "o2" | tee filtr1

# Přesunutí souboru zk3
mv zk3 /STUDENT/vypis

# Opětovné nastavení práv (často se dělá pro jistotu)
sudo chmod -R 777 /STUDENT

# Výpis adresáře STUDENT (v kořenovém adresáři)
ls -l /STUDENT

# Smazání celého adresáře /STUDENT (rekurzivně a nuceně)
sudo rm -r /STUDENT

# Smazání zástupce/složky na ploše (pokud vznikla)
# Pozn: Tento příkaz je pravděpodobně chyba, pokud /STUDENT nebyl na ploše
sudo rm -r ~/Plocha/STUDENT

Test,Popis
cislo1 -eq cislo2,Čísla 1 a 2 se rovnají (equal)
cislo1 -ne cislo2,Čísla se nerovnají (not equal)
cislo1 -lt cislo2,Číslo 1 je menší než číslo 2 (less than)
cislo1 -le cislo2,Číslo 1 je menší nebo rovno (less or equal)
cislo1 -gt cislo2,Číslo 1 je větší než číslo 2 (greater than)
cislo1 -ge cislo2,Číslo 1 je větší nebo rovno (greater or equal)
