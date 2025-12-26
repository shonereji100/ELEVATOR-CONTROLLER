# ELEVATOR-CONTROLLER
SA finite state machine–based Verilog HDL elevator controller for a three-floor system. Handles cabin and hall requests, models realistic travel and door timing using counters, and returns to an idle floor after servicing. Includes a complete simulation testbench.
This project implements a single-user elevator controller for a three-floor building using Verilog HDL. The elevator services Floor 0, which acts as the idle floor, along with Floor 1 and Floor 2. The system is designed to mimic realistic elevator behavior by accepting both inside (cabin) and outside (hall) button requests, moving to the requested destination floor, opening the doors for a fixed duration, and automatically returning to Floor 0 after the passenger is dropped off.

---

## 🧠 Design Architecture

### 📨 Request Handler
The request handler monitors both cabin and hall button inputs and captures a single active request at a time. Based on the selected destination and the current floor, it determines the required direction of travel. No additional requests are accepted until the current request is fully serviced.

---

### 🚆 Movement Controller
The movement controller governs elevator motion between floors. Instead of using physical floor sensors, it relies on counter-based timing to model travel between floors. The controller drives upward or downward movement and signals arrival once the configured travel time elapses.

---

### 🚪 Door Controller
The door controller manages door opening and closing operations. Upon reaching the destination floor, the doors are opened for a fixed duration defined by a timing parameter. After the door-open interval expires, the doors close automatically, and control returns to the idle or return state.

---

## 🏢 Floor & Button Configuration
- **Floor 0 (Idle Floor):** UP button only  
- **Floor 1:** UP and DOWN buttons  
- **Floor 2:** DOWN button only  

**Cabin Buttons:** Floor 0, Floor 1, Floor 2  

---

## 👥 **Project By**
**1) Shone Reji**  
**2) Jovine Binesh**  
**3) George Amal Renju**  
**4) Nandagopal R**  
**5) Aswin Santhosh**


