# ha-solarman-custom_components-solarman-inverter_definitions-all_in_one_betteress_srne

# Home Assistant Solarman Definition: BetterESS All-in-One / SRNE ASP48100SH3 (10kW 3-Phase)

Custom inverter definition file (`all_in_one_betteress_srne.yaml`) for the **Home Assistant Solarman** integration. Designed specifically for the **BetterESS All-in-One** energy storage system based on the **SRNE ASP48100SH3** 10kW three-phase hybrid inverter.

*(Polska wersja instrukcji znajduje się poniżej / Polish instructions below)*

---

## 🇬🇧 English

### Why this file?
Standard `srne.yaml` definitions available in Solarman integrations often have mismatched or missing Modbus registers for the **BetterESS** / **SRNE ASP48100SH3** 3-phase hybrid inverter. This profile has been manually mapped and verified against the SRNE Modbus Protocol v1.96.

### Supported Features
* **Battery Monitoring:** SOC (%), Voltage, Current, and real-time Charge/Discharge Power.
* **PV Inputs (2x MPPT):** Voltage, Current, and Power for PV1 and PV2.
* **3-Phase Grid & Load (L1, L2, L3):** Phase voltages, currents, active power, apparent power, grid frequency, and inverter temperatures.
* **Energy Meters:** Daily and total PV production, grid energy import, load consumption, and battery charge/discharge (Ah).
* **Full Remote Control (Settings):**
  * SOC cutoffs and switching thresholds (Utility / Inverter / Alarm).
  * Max battery charging current & max utility charging current.
  * Output source priority (`SOL`, `UTI`, `SBU`, `SUB`) and charging mode (`OSO`, `SNU`).
  * Grid export control (`Feed Back Hybrid`: Disable / On-Grid).
  * Time-of-Use (TOU) charging and discharging schedules.

### Installation
1. Download the `all_in_one_betteress_srne.yaml` file from this repository.
2. Copy it to your Home Assistant `inverter_definitions` directory (path depends on the Solarman integration version you use):
   * `config/custom_components/solarman/inverter_definitions/`
3. Restart Home Assistant.
4. Go to **Settings -> Devices & Services -> Solarman**, reconfigure your inverter, and select **`all_in_one_betteress_srne.yaml`** from the inverter definition list.

---

## 🇵🇱 Polski

### Dlaczego powstał ten plik?
Domyślne definicje `srne.yaml` dostępne w integracjach Solarman nie pokrywają się z mapą rejestrów trójfazowego falownika hybrydowego **BetterESS All-in-One (SRNE ASP48100SH3 10kW)**. Ten plik został ręcznie opracowany i przetestowany w oparciu o dokumentację protokołu SRNE Modbus v1.96.

### Obsługiwane funkcje
* **Magazyn energii (Bateria):** Poziom naładowania SOC (%), napięcie, natężenie prądu oraz moc ładowania/rozładowania w czasie rzeczywistym.
* **Panele fotowoltaiczne (2x MPPT):** Odczyt napięcia, prądu i mocy osobno dla stringów PV1 oraz PV2.
* **Sieć i odbiory 3-fazowe (L1, L2, L3):** Napięcia i prądy na każdej fazie, moc czynna i pozorna obciążenia (`Load`), częstotliwość sieci oraz temperatury falownika.
* **Liczniki energii:** Dzienna i całkowita produkcja PV, pobór energii z sieci, zużycie domu oraz bilans ładowania/rozładowania baterii (w Ah).
* **Zdalne sterowanie falownikiem z Home Assistant:**
  * Ustawianie progów procentowych SOC (przełączanie na sieć, powrót na baterię, odcięcie rozładowania, alarm).
  * Regulacja maksymalnego prądu ładowania baterii oraz prądu ładowania z sieci.
  * Zmiana priorytetu źródła zasilania (`SOL`, `UTI`, `SBU`, `SUB`) i trybu ładowania (`OSO`, `SNU`).
  * Włączanie/wyłączanie eksportu energii do sieci (`Feed Back Hybrid`).
  * Harmonogramy czasowe ładowania i rozładowywania magazynu energii.

### Instrukcja instalacji w Home Assistant
1. Pobierz plik `all_in_one_betteress_srne.yaml` z tego repozytorium.
2. Wgraj go do folderu z definicjami falowników w swoim Home Assistant (np. przez Samba Share lub File Editor):
   * `config/custom_components/solarman/inverter_definitions/`
3. Zrestartuj Home Assistanta.
4. Wejdź w **Ustawienia -> Urządzenia oraz usługi -> Solarman**, kliknij **Konfiguruj** przy swoim falowniku i wybierz z listy plik **`all_in_one_betteress_srne.yaml`**.



<img width="1206" height="2349" alt="IMG_7771" src="https://github.com/user-attachments/assets/a1700460-4da7-4a42-b85b-4879d0106d0c" />

<img width="1206" height="1556" alt="IMG_7770" src="https://github.com/user-attachments/assets/5a04bc99-5128-40b7-8faa-676c16bb479a" />

BetterESS (off-grid) + Sofar Solar (on-grid)

<img width="1206" height="1614" alt="IMG_7762" src="https://github.com/user-attachments/assets/21292002-530c-4b15-8e99-38a521f4da6c" />

