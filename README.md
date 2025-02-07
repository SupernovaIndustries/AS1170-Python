# AS1170 Python Library

## Descrizione
Questa libreria permette di controllare il driver **AS1170** via **I2C** su **Raspberry Pi**, gestendo i LED con comandi semplici come `led1.on()` e `led1.off()`.

## Installazione
Poiché Raspberry Pi OS utilizza una gestione dei pacchetti più restrittiva, si consiglia di installare la libreria in un ambiente virtuale per evitare conflitti.

### 1️⃣ Installare Python Virtual Environment
Se non hai già `venv` installato, esegui:
```sh
sudo apt install python3-venv
```

### 2️⃣ Creare un Virtual Environment
All'interno della cartella del progetto:
```sh
python3 -m venv venv
```

### 3️⃣ Attivare il Virtual Environment
```sh
source venv/bin/activate
```

### 4️⃣ Installare la libreria
```sh
pip install .
```

Se vuoi installare in modalità **sviluppatore** (per modificare il codice senza reinstallare):
```sh
pip install -e .
```

### 5️⃣ Utilizzare la libreria
```python
from as1170.driver import led1, led2

led1.on()
time.sleep(1)
led1.off()
```

### 6️⃣ Uscire dal Virtual Environment
```sh
deactivate
```

## Installazione Senza Virtual Environment (Opzionale)
Se vuoi installare la libreria globalmente, puoi forzare `pip` con:
```sh
pip install . --break-system-packages
```
⚠ **Attenzione:** Questo potrebbe causare problemi con i pacchetti di sistema. È consigliato usare un **virtual environment**.

---

## Controllo dei LED
Dopo aver installato la libreria, puoi controllare i LED come segue:

```python
from as1170.driver import led1, led2

led1.on()  # Accende il LED1
led2.on()  # Accende il LED2

led1.off() # Spegne il LED1
led2.off() # Spegne il LED2
```

## Disinstallazione
Per rimuovere la libreria dal tuo ambiente virtuale:
```sh
pip uninstall as1170
```
Se vuoi eliminare completamente l'ambiente virtuale:
```sh
rm -rf venv
```

