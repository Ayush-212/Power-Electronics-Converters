## 📖 Theory of Operation

Both circuits operate as switch-mode power supplies (SMPS). They use a semiconductor switch (like a MOSFET), a diode, and an LC filter (inductor and capacitor) to transfer and regulate power efficiently by alternating between two distinct states.

---

### 📉 1. Buck Converter (Step-Down)
The Buck converter reduces a higher input voltage ($V_{in}$) to a lower, regulated output voltage ($V_{out}$). 

#### 🔄 Operating States
* **Switch ON ($T_{on}$):** The switch closes. Current flows from the input source through the inductor to the load, storing energy in the inductor's magnetic field. The voltage across the inductor is:
  $$V_L = V_{in} - V_{out}$$
* **Switch OFF ($T_{off}$):** The switch opens. The inductor resists the sudden drop in current, flipping its voltage polarity. This forces the diode to turn on (freewheeling), allowing the stored magnetic energy in the inductor to discharge into the load. The voltage across the inductor is:
  $$V_L = -V_{out}$$

#### 📐 Conversion Formula
Based on the inductor volt-second balance, the ideal output voltage is directly proportional to the duty cycle ($D$):
$$V_{out} = D \cdot V_{in}$$

---

### 📈 2. Boost Converter (Step-Up)
The Boost converter steps up a lower input voltage ($V_{in}$) to a higher, regulated output voltage ($V_{out}$).

#### 🔄 Operating States
* **Switch ON ($T_{on}$):** The switch closes, connecting the output side of the inductor directly to ground. Current flows from the input through the inductor to ground, storing energy heavily in the inductor's magnetic field. During this time, the output capacitor alone supplies power to the load. The voltage across the inductor is:
  $$V_L = V_{in}$$
* **Switch OFF ($T_{off}$):** The switch opens. The inductor's magnetic field collapses, forcing its voltage polarity to flip. This voltage stacks on top of the input voltage ($V_{in} + V_L$), pushing energy through the diode to charge the output capacitor and feed the load. The voltage across the inductor is:
  $$V_L = V_{in} - V_{out}$$

#### 📐 Conversion Formula
Because energy is only transferred to the output when the switch is open, the output voltage is inversely proportional to the switch off-time:
$$V_{out} = \frac{V_{in}}{1 - D}$$
