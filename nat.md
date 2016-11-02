class: middle, center
# Enterprise/Carrier-Grade NAT at UiT
## A BSD lovestory...

---

# Agenda
- Components
- Wiring
- Configuration
- Uses

---
# Components
- Routers
- Plain(Pizzabox) server
- OpenBSD
- CARP/HSRP

# Wiring
- NAT-box at each core router
-- Kept in sync over a dedicated VLAN for pfSync
- Policy-based routing on edge routers to steer traffic
- Rules on NAT boxes

#Thank you!
- Questions?
