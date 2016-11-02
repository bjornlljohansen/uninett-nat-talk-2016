class: middle, center
# Enterprise/Carrier-Grade NAT at UiT
## A BSD lovestory...
### Bjørn Johansen <bjorn.l.johansen@uit.no>
---

# Agenda
- Outline
- Components
- Wiring
- Configuration
- Uses

---

# Outline
- RFC1918-adresses on 4 campuses translated
- Cheap(~$10000) solution with geo-redundancy and 10Gbps capacity(potential for bundling)
- 1U Dell server

---

# Components
- Routers
- Plain(Pizzabox) server
- OpenBSD
- CARP/HSRP

---

# Wiring
- NAT-box at each core router
    - Kept in sync over a dedicated VLAN for pfSync
- Policy-based routing on core routers to steer traffic towards the NAT-solution
    - All major campuses
- Rules on NAT boxes

---

#Configuration
- Plain pf configuration(with OpenBSD spice)
- Custom SNMP OID's
    - Plans for use of UiT PEN assigned by IANA
---

#Statistics
- Peak of 120k translations/s on an average day
- Peak of 2.5k internal addresses translated
- Peak of 95k states on average day
- 99.2% idle :P
---

# Future plans and improvements
- RESTful management
    - Integration into NAV DHCP module
	- Temporarily NAT individual adresses on demand
    - Eyecandy and dashboard
    - External Address usage

- Potential for small NUC appliance
- Usage within wireless/wired performance monitoring
    - Look at TCP restransmissions, ACKs

---

#Thank you!
- Questions?
