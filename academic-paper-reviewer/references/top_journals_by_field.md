# Top Venues by Field — Networking, Security & Systems

This document is used by `field_analyst_agent` and `eic_agent` as a reference for calibrating the Journal-Fit Reviewer identity and assessing venue fit.

**Ranking systems referenced:**
- **CCF** = Chinese Computer Society, 7th Edition (2026)
- **115年** = NYCU College of Computer Science (資工學院) 115年 top/important international conference list, dated 2026-03-23 (`Top-conf-List-20260323.xlsx`, sheets 國際會議等級A + 國際會議等級B). The full list, all CS areas, is in [`top_conf_list_115.csv`](top_conf_list_115.csv) (columns: `level` A/B, `area`, `no`, `venue`, citations, `note` = 教評會 approval date). Tables below last refreshed against it 2026-04-23.
- **Inst.** = Institutional doctoral program grading (115年 conference list + 博士班期刊論文類別認定辦法 113.01.09):

| Code | Rule |
|------|------|
| 會議等級A | On the 115年 等級A (頂尖) sheet |
| 會議等級B | On the 115年 等級B (重要) sheet |
| 會議等級C | Other peer-reviewed conference |
| 期刊A類 | JCR Q1 (top 25%) in any non-Neg-JCR-c category, and not on Neg-A / Neg-B |
| 期刊B類 | JCR Q1+Q2 (top 50%), and not on Neg-B |
| 期刊C類 | Other SCI / SCIE / EI / SSCI / A&HCI journal |

Neg-A (never 期刊A類, whatever the JCR quartile) includes IEEE Access, Scientific Reports, PLOS ONE, Heliyon, SAGE Open; the full Neg-A / Neg-B lists are in the appendix of the 認定辦法. A poster at a 頂尖 venue counts at 50% only with a program-chair letter stating oral/poster was not split by quality and a full-length paper in the proceedings (102.3.20 教評會).

**Cross-check reminder:** The 115年 list only has 等級A (頂尖) and 等級B (重要) sheets. Any venue not on either sheet is either (a) 會議等級C under institutional rules, or (b) not institutionally recognised. NSDI, for instance, is **not in 115年 list** — counts as 等級C under strict institutional rules despite CCF-A.

---

## 1. Computer Networking — Journals

### Tier A (Top)

| Abbrev. | Journal | Publisher | CCF | Inst. | Notes |
|---------|---------|-----------|-----|-------|-------|
| JSAC | IEEE Journal on Selected Areas in Communications | IEEE | A | 期刊A類 (JCR Q1) | Thematic issues; networking flagship |
| TMC | IEEE Transactions on Mobile Computing | IEEE | A | 期刊A類 (JCR Q1) | Mobile + satellite transport |
| TON | IEEE Transactions on Networking (formerly IEEE/ACM ToN) | IEEE | A | 期刊A類 (JCR Q1) | Primary networking journal |

### Tier B

| Abbrev. | Journal | Publisher | CCF | Inst. | Notes |
|---------|---------|-----------|-----|-------|-------|
| TOIT | ACM Transactions on Internet Technology | ACM | B | — | Internet architecture, protocols |
| TOSN | ACM Transactions on Sensor Networks | ACM | B | — | IoT, sensor networking |
| CN | Computer Networks | Elsevier | B | 期刊B類 (JCR Q2) | Broad networking; survey-friendly |
| TCOM | IEEE Transactions on Communications | IEEE | B | — | Physical + network layer comms |
| TWC | IEEE Transactions on Wireless Communications | IEEE | B | — | Wireless, satellite links |

### Tier C

| Abbrev. | Journal | Publisher | CCF | Inst. | Notes |
|---------|---------|-----------|-----|-------|-------|
| CC | Computer Communications | Elsevier | C | 期刊B類 (JCR Q2) | LEO routing, transport |
| TNSM | IEEE Trans. on Network and Service Management | IEEE | C | 期刊B類 (JCR Q2) | SDN/NFV management, P4 |
| JNCA | Journal of Network and Computer Applications | Elsevier | C | 期刊B類 (JCR Q2) | Applied networking |
| IoT-J | IEEE Internet of Things Journal | IEEE | C | 期刊A類 (JCR Q1) | IoT + satellite IoT |
| MONET | Mobile Networks and Applications | Springer | C | — | Mobile, satellite |
| WCMC | Wireless Communications and Mobile Computing | Wiley | C | — | — |
| Ad Hoc | Ad Hoc Networks | Elsevier | C | — | Self-organizing networks |

> **Note:** IoT-J is CCF-C but JCR Q1, qualifying as 期刊A類 under institutional rules. TNSM/CN/JNCA/CC are CCF-B/C but JCR Q2, qualifying as 期刊B類.

---

## 2. Computer Networking — Conferences

### Tier A (Top)

| Abbrev. | Conference | Org. | CCF | 115年 | Inst. | Notes |
|---------|-----------|------|-----|-------|-------|-------|
| SIGCOMM | ACM SIGCOMM | ACM | A | 頂尖 | 會議等級A | Premier networking venue |
| INFOCOM | IEEE INFOCOM | IEEE | A | 頂尖 | 會議等級A | Largest networking conference |
| MobiCom | ACM MobiCom | ACM | A | 頂尖 | 會議等級A | Mobile computing + networking |
| NSDI | USENIX NSDI | USENIX | A | **not on 115年 list** | 會議等級C (strict) / A (community) | CCF-A but institution 不認列；advisor may override |
| MobiHoc | ACM MobiHoc | ACM/IEEE | B | 頂尖 | 會議等級A | Ad hoc + mobile theory (institution counts as 頂尖) |
| SIGMETRICS | ACM SIGMETRICS / POMACS | ACM | B* | 頂尖 | 會議等級A | Measurement + performance (*CCF-B in systems, 會議A per institution) |

### Tier B (Important)

| Abbrev. | Conference | Org. | CCF | 115年 | Inst. | Notes |
|---------|-----------|------|-----|-------|-------|-------|
| SenSys | ACM SenSys | ACM | B | 重要 | 會議等級B | Embedded sensor systems (115年 marks 重要, not 頂尖) |
| CoNEXT | ACM CoNEXT | ACM | B | **not on 115年 list** | 會議等級C (strict) | Emerging networking; CCF-B but not institutionally listed |
| ICNP | IEEE ICNP | IEEE | B | 重要 | 會議等級B | Network protocols |
| MobiSys | ACM MobiSys | ACM | B | 重要 | 會議等級B | Mobile systems |
| IMC | ACM IMC | ACM/USENIX | B | — | — | Internet measurement (not on 115年 list) |
| IWQoS | IEEE/ACM IWQoS | IEEE | B | — | — | Quality of service |
| IPTPS | USENIX Peer-to-Peer Systems | USENIX | — | 重要 | 會議等級B | Per 115年 (line 67 of 等級B sheet); note: venue defunct since 2010, historical record |

### Tier C (Peer-Reviewed)

| Abbrev. | Conference | Org. | CCF | 115年 | Inst. | Notes |
|---------|-----------|------|-----|-------|-------|-------|
| GLOBECOM | IEEE GLOBECOM | IEEE | C | 重要 | 會議等級B | Large IEEE comms venue (108.07.25 institutional approval). Annual Dec. |
| ICC | IEEE ICC | IEEE | C | 重要 | 會議等級B (Oral only) | International comms (102.6.20 approval; only Oral papers count) |
| NOMS | IEEE/IFIP NOMS + IM | IEEE/IFIP | C | 重要 | 會議等級B | Network operations & management (113.01.09 approval) |
| WCNC | IEEE WCNC | IEEE | C | 重要 | 會議等級B | Wireless comms |
| **HPSR** | **IEEE HPSR** | **IEEE** | — | **重要** | **會議等級B** | **High Performance Switching and Routing (112.05.15 approval). Directly relevant to P4/programmable data-plane / switching papers.** |
| LCN | IEEE LCN | IEEE | C | — | — | Local computer networks |
| ISCC | IEEE ISCC | IEEE | C | — | — | Symposium on computers & comms |
| APNet | ACM APNet | ACM | C | — | 會議等級C | Asia-Pacific networking workshop |
| HotNets | ACM HotNets | ACM | C | — | — | Vision papers, networking |
| MSN | IEEE MSN | IEEE | C | — | — | Mobility, sensing, networking |

---

## 3. Network & Information Security — Journals

### Tier A

| Abbrev. | Journal | Publisher | CCF | Inst. | Notes |
|---------|---------|-----------|-----|-------|-------|
| TDSC | IEEE Trans. on Dependable and Secure Computing | IEEE | A | 期刊A類 | Dependability + security |
| TIFS | IEEE Trans. on Information Forensics and Security | IEEE | A | 期刊A類 | Digital forensics, network security |
| JoC | Journal of Cryptology | Springer | A | — | Theoretical cryptography |

### Tier B

| Abbrev. | Journal | Publisher | CCF | Inst. | Notes |
|---------|---------|-----------|-----|-------|-------|
| TOPS | ACM Trans. on Privacy and Security | ACM | B | — | Privacy, access control |
| C&S | Computers & Security | Elsevier | B | 期刊A類 (JCR Q1) | Applied security; P4/SmartNIC security |

### Tier C

| Abbrev. | Journal | Publisher | CCF | Notes |
|---------|---------|-----------|-----|-------|
| SCN | Security and Communication Networks | Wiley | C | Network security |
| CLSR | Computer Law & Security Review | Elsevier | C | Policy + legal |
| HCC | High-Confidence Computing | Elsevier | C | Trustworthy computing |

---

## 4. Network & Information Security — Conferences

### Tier A

| Abbrev. | Conference | Org. | CCF | 115年 | Inst. |
|---------|-----------|------|-----|-------|-------|
| S&P | IEEE Symposium on Security and Privacy | IEEE | A | 頂尖 | 會議等級A |
| CCS | ACM CCS | ACM | A | 頂尖 | 會議等級A |
| USENIX Security | USENIX Security Symposium | USENIX | A | 頂尖 | 會議等級A |
| CRYPTO | International Cryptology Conference | Springer | A | 頂尖 | 會議等級A |
| EUROCRYPT | EUROCRYPT | Springer | A | 頂尖 | 會議等級A |
| NDSS | Network and Distributed System Security | ISOC | A | 重要 | 會議等級B |
| DSN | IEEE/IFIP DSN | IEEE | — | 頂尖 | 會議等級A |

### Tier B–C

| Abbrev. | Conference | Org. | CCF | Notes |
|---------|-----------|------|-----|-------|
| ACSAC | Annual Computer Security Applications Conf. | IEEE | B | Applied security |
| ASIACCS | ACM AsiaCCS | ACM | — | 會議等級B (inst.) |
| RAID | RAID Symposium | — | B | Intrusion detection |
| BlackSeaCom | IEEE BlackSeaCom | IEEE | — | Regional; P4/SmartNIC security papers |
| CNSM | IEEE CNSM | IEEE | — | Network/service management + security |

---

## 5. Computer Systems & Operating Systems (Selected)

### Tier A Conferences

| Abbrev. | Conference | Org. | CCF | 115年 | Inst. |
|---------|-----------|------|-----|-------|-------|
| OSDI | USENIX OSDI | USENIX | A | 頂尖 | 會議等級A |
| SOSP | ACM SOSP | ACM | A | 頂尖 | 會議等級A |
| USENIX ATC | ACM SIGOPS ATC | ACM | A | 頂尖 (listed as "USENIX Technical Conference") | 會議等級A |
| EuroSys | ACM EuroSys | ACM | A | 頂尖 | 會議等級A |

### Tier A–B Journals

| Abbrev. | Journal | Publisher | CCF | Notes |
|---------|---------|-----------|-----|-------|
| TOCS | ACM Trans. on Computer Systems | ACM | A | Systems flagship |
| TPDS | IEEE Trans. on Parallel and Distributed Systems | IEEE | A | Distributed systems |
| ACM CSUR | ACM Computing Surveys | ACM | — | 期刊A類; survey venue |

### Tier B–C Conferences (relevant to research)

| Abbrev. | Conference | Org. | CCF | Notes |
|---------|-----------|------|-----|-------|
| ICDCS | IEEE ICDCS | IEEE | B | Distributed computing; 會議等級A (inst.) |
| PODC | ACM PODC | ACM | B | Distributed computing theory; 會議等級A (inst.) |
| NFV-SDN | IEEE NFV-SDN | IEEE | — | SDN/NFV; 會議等級C |
| EuroP4 | EuroP4 Workshop (CoNEXT) | ACM | — | P4-specific workshop |

---

## 6. Aerospace & Transport (Cross-Domain)

| Abbrev. | Journal | Publisher | CCF | Inst. | Notes |
|---------|---------|-----------|-----|-------|-------|
| TAES | IEEE Trans. on Aerospace and Electronic Systems | IEEE | — | 期刊B類 (JCR Q2) | LEO satellite systems |
| CJA | Chinese Journal of Aeronautics | Elsevier | — | 期刊B類 (JCR Q2) | Aerospace engineering |
| Space: S&T | Space: Science & Technology | AAAS/BAS | — | 期刊C類 | LEO constellation design |
| Aerospace | Aerospace (MDPI) | MDPI | — | 期刊C類 | Satellite thermal/systems |
| Scientific Reports | Scientific Reports | Nature | — | 期刊C類 (Neg-A) | Broad; NOT 期刊A despite Nature |
| IEEE Access | IEEE Access | IEEE | — | 期刊C類 (Neg-A) | Open access; downgraded |

> **Neg-A warning:** IEEE Access and Scientific Reports are on the institutional negative list — they cannot count as 期刊A類 regardless of JCR quartile.

---

## 7. Interdisciplinary / High-Impact

| Journal | Publisher | IF Range | Notes |
|---------|-----------|---------|-------|
| *Nature* | Springer Nature | 50–70 | Highest standards; all natural sciences |
| *Science* | AAAS | 45–65 | All natural sciences |
| *Nature Communications* | Springer Nature | 14–17 | Broad scope, open access |
| *PNAS* | NAS | 10–12 | Interdisciplinary research |
| *IEEE Communications Magazine* | IEEE | 8–10 | Networking vision/tutorials |
| *ACM SIGCOMM CCR* | ACM | — | Networking community newsletter; short papers |
| *IEEE Network* | IEEE | 8–10 | Networking magazine |
| *IEEE Communications Surveys & Tutorials (COMST)* | IEEE | 30+ | Survey venue; 期刊A類 (JCR Q1) |

---

## Usage Guide

### Three-System Cross-Reference Logic

When assessing a paper's venue quality, check all three ranking systems:

1. **CCF grade (A/B/C):** International community consensus
2. **115年 institutional list (頂尖/重要):** Determines doctoral credit at the user's institution
3. **Inst. grade (會議A/B/C, 期刊A/B/C):** Aligned with JCR quartile + negative lists (rules at the top of this file)

### Logic for Selecting Journals for the Journal-Fit Reviewer

- If the paper targets CCF-A + 會議等級A → assign the Journal-Fit Reviewer persona from that venue (e.g., SIGCOMM TPC chair persona)
- If CCF-B or 會議等級B → assign the persona from a strong B-tier venue (e.g., GLOBECOM area editor)
- If the paper is a survey → prefer ACM CSUR or IEEE COMST persona

### Key Discrepancies Between Systems

| Venue | CCF | Inst. | Explanation |
|-------|-----|-------|-------------|
| SIGMETRICS/POMACS | B (Systems) | 會議等級A | Institution counts it as top-tier networking |
| NDSS | A (Security) | 會議等級B | Institution rates it below S&P/CCS |
| ICC/GLOBECOM | C | 會議等級B | Institution rates them higher than CCF |
| IoT-J | C | 期刊A類 | JCR Q1 overrides CCF-C under institutional rules |
| IEEE Access | — | 期刊C類 (Neg-A) | On negative list; cannot be 期刊A regardless of IF |

### Notes

- This list focuses on **Networking, Security, Systems, and Aerospace** — the user's research domains (P4, SDN, LEO satellite, QUIC, SmartNIC, fast reroute)
- Impact Factors are approximate and fluctuate yearly
- For fields not listed here, consult the full CCF 7th Edition directory or [`top_conf_list_115.csv`](top_conf_list_115.csv)
