# ScrapTrap – Didactic HTTP Header & Web Security Audit Framework

[ 🇬🇧 English Documentation ](#english) | [ 🇩🇪 Deutsche Dokumentation ](#deutsch)

---

<a name="english"></a>
## 🇬🇧 English Documentation

ScrapTrap is a research‑grade, context‑aware HTTP header and web security audit engine designed for deep diagnostics, didactic clarity, and empirical analysis.
It bridges the gap between abstract security protocols and real‑world server administration by providing high‑resolution insights, contextual risk evaluation, and actionable remediation guidance.

Unlike standard automated scanners, ScrapTrap focuses on education, explainability, and architectural correctness — making it ideal for research, teaching, and high‑risk public‑facing infrastructure.

---

### 🔬 Core Purpose: Research & Didactics

ScrapTrap is built for environments where misconfigurations matter more than exploits, and where trust boundaries are critical:

* **Empirical Security Studies:** Used in ongoing research analyzing security posture and misconfiguration vectors of high‑risk NGO websites (e.g., women’s shelters, crisis counseling, health support networks).
* **Actionable Education:** Every finding includes a detailed, context‑aware explanation and step‑by‑step remediation guidance for administrators.
* **Configuration Drift Detection:** Exposes hidden structural flaws that commercial scanners routinely overlook — especially in legacy or volunteer‑maintained systems.

---

### ⚙️ Technical Feature Overview (Full Scope)

ScrapTrap performs a comprehensive, multi‑layered audit of HTTP headers, server behavior, HTML structures, and root‑level files.

#### Security & Performance Header Analysis
* SSL/HTTPS validation
* CSP, HSTS, Permissions‑Policy, Referrer‑Policy
* X‑Frame‑Options, X‑Content‑Type‑Options, X‑XSS‑Protection
* Cache‑Control, Pragma, Expires, ETag
* 227 distinct HTTP headers checked

#### Proxy / CDN / WAF Fingerprinting
* Cloudflare, Akamai, Fastly, Myra, Imperva, Sucuri
* AWS ELB, Azure Front Door, Google Cloud CDN
* Varnish, HAProxy, Traefik, OpenResty
* Silent bot‑mitigation layers
* Reverse proxy chain detection

#### Client‑Hints & Bot‑Protection Detection
* Accept‑CH, Critical‑CH
* CF‑Mitigated
* Speculation-Rules & Prerendering Detection (Speculation Rules API)
* Advanced bot‑blocking heuristics

#### Redirect & Domain Integrity Checks
* HTTPS enforcement
* www/non‑www consistency
* Redirect chain analysis
* Soft‑404 detection

#### Consent‑Relevant Third‑Party Detection
*(No legal advice)*
* Google Fonts
* Google Tag Manager
* Microsoft Clarity
* Other third‑party embeds

#### HTML / Meta / Server Cross‑Validation
* Mapping HTML `<meta http-equiv>` to real server headers
* Automatic `.htaccess` generation
* Canonical tag validation
* Language & OpenGraph checks

#### CMS / Shop System Fingerprinting (100+ systems)
* WordPress, Joomla, Drupal, TYPO3
* Magento, Shopware, PrestaShop, Shopify
* Ghost, Next.js, Nuxt, Express
* Laravel, Symfony, Django, Flask
* Obscurity‑Check for server leaks

#### Root‑Level File Diagnostics
* `robots.txt`
* `llms.txt`
* `llms-fulltext.txt`
* `security.txt`
* `infophp.php`
* Multiple index root files (`.php`, `.html`, `.htm`)

#### Isolation & Obfuscation Analysis (Quarantine Engine)
* Zero‑Regex engine
* Score‑based detection of obfuscation, loaders, hidden payloads
* Safe filtering of suspicious code fragments

#### E‑Mail Security Validation
* MX, SPF, DKIM, DMARC
* BIMI (non‑security, informational)

#### User‑Agent Testing
* 19 selectable UAs
* Detection of simple UA‑blocking mechanisms

#### Legacy Compatibility
* Fully compatible with PHP 4.3
* Conforms to ScrapTrap Framework Policy

---

### 🚀 Unique Engine Features

#### 227‑Point Zero‑Regex Engine
* Deterministic parsing
* Memory‑safe
* No catastrophic backtracking
* Extremely fast execution
* Ideal for malformed or adversarial input

#### Context‑Aware Risk Matrix (detailed via page-type tooltips)
Severity adapts to:
* NGO / sensitive topic
* E‑Commerce
* Blog / Magazine
* Private site
* API / Headless

#### Soft‑404 Entrapment
Detects servers returning HTML error pages with `200 OK`.

#### Crawler Instruction Validation
Checks:
* `robots.txt`
* `llms.txt`
* `llms-fulltext.txt`
* `infophp.php`
* `security.txt`

#### Infrastructure Fingerprinting
Unmasks:
* WAFs
* CDNs
* Reverse proxies
* Load balancers
* Bot‑mitigation layers

---

### 🏛️ Architectural Guarantees (Privacy‑First by Design)

ScrapTrap follows a strict privacy‑first, zero‑exposure architecture designed for maximum transparency, minimal attack surface, and complete independence from external services.

* **No Database:** No audited data is stored, logged, persisted, or written to disk. All audits run fully in‑memory and are discarded immediately.
* **No Cloud Dependencies:** No external APIs, cloud services, or telemetry endpoints. The engine operates entirely on the ScrapTrap server without third‑party calls.
* **No JavaScript Execution:** ScrapTrap does not execute client‑side JavaScript. Prevents script‑based fingerprinting, tracking, or side‑effects.
* **No Tracking:** No analytics, cookies, behavioral profiling, or user identification. ScrapTrap does not track domains, usage patterns, or audit history.
* **No Telemetry:** No metrics, no usage reporting, no external monitoring. The system is completely opaque to third parties.
* **No Advertising:** No banners, no affiliate links, no commercial injections. ScrapTrap is a pure diagnostic and didactic tool.
* **No Exploit Execution:** ScrapTrap never performs penetration testing, brute‑force attempts, or CVE exploitation. It is strictly a read‑only diagnostic engine.

---

### 📊 Ongoing Empirical Project: Vulnerability Vectors in High-Risk NGO Infrastructures

This framework is actively utilized as the primary diagnostic instrument for an ongoing empirical security study. The project monitors and analyzes the baseline technical security posture of public-facing web infrastructure within highly sensitive NGO fields (specifically focusing on **women’s shelters (Frauenhäuser)**, **crisis counseling networks**, and **HIV/AIDS support organizations (Aidshilfe)**).

*   **The Problem:** Entities operating in these fields handle high-consequence data, where configuration drifts or architectural leaks can directly compromise human safety and vulnerable identities.
*   **Current Research Insights:** Preliminary data extracted via this diagnostic engine reveals an alarming, widespread vulnerability surface within the non-profit sector. Major systemic failures include catastrophic omissions of modern Content Security Policies (CSP), complete absence of clickjacking protections, and unmitigated server-header leaks that expose underlying patch-levels to automated reconnaissance tools.
*   **Anonymization Strategy:** To preserve the security of the monitored entities, all research findings, percentage matrices, and structural vulnerability statistics are completely anonymized and stripped of targeting identifiers before academic mapping.


---

### 🌐 Live Access

🔗 [https://scraptrap.de/scraptrap_http_header_audit.php](https://scraptrap.de/scraptrap_http_header_audit.php)

---

### ⚠️ Intellectual Property Notice

The underlying parser logic, heuristics, and diagnostic engine are proprietary components of the ScrapTrap Bot Mitigation & WAF Framework.  
This repository provides documentation, research context, and didactic materials — not the source code of the core engine.

---

<a name="deutsch"></a>
## 🇩🇪 Deutsche Dokumentation

# ScrapTrap – Didaktisches HTTP-Header & Web-Security-Audit-Framework

ScrapTrap ist eine kontextsensitive Audit-Engine für HTTP-Header und Web-Sicherheit auf Research-Niveau, entwickelt für ausführliche Diagnosen, didaktische Klarheit und empirische Analysen.  
Die Anwendung schließt die Lücke zwischen abstrakten Sicherheitsprotokollen und der praktischen Serveradministration, indem sie hochauflösende Einblicke, kontextbezogene Risikobewertungen und konkrete Handlungsempfehlungen liefert.

Im Gegensatz zu herkömmlichen automatisierten Scannern konzentriert sich ScrapTrap auf Vermittlung, Erklärbarkeit und architektonische Korrektheit, was die Brauchbarkeit für Forschung, Lehre und sensiblere, öffentlich zugängliche Infrastrukturen erhöht.

---

### 🔬 Kerngedanke: Forschung & Didaktik

ScrapTrap wurde für Umgebungen entwickelt, in denen Fehlkonfigurationen schwerer wiegen als Exploits und in denen Vertrauensgrenzen kritisch sind:

* **Empirische Sicherheitsstudien:** Eingesetzt in laufenden Forschungsprojekten zur Analyse des Sicherheitsniveaus und von Fehlkonfigurationsvektoren auf Webseiten von High-Risk-NGOs (z. B. Frauenhäuser, Krisenberatungen, Gesundheitshilfenetzwerke).
* **Praxisnahe Vermittlung:** Jeder Befund enthält eine detaillierte, kontextsensitive Erklärung sowie z.T. Schritt-für-Schritt-Anleitungen zur Behebung für Administrator:innen.
* **Erkennung von Configuration Drift:** Deckt verborgene strukturelle Schwachstellen auf, die kommerzielle Scanner häufig übersehen, insbesondere in Altsystemen oder von Ehrenamtlichen gewarteten Systemen.

---

### ⚙️ Technische Feature-Übersicht (Gesamtumfang)

ScrapTrap führt ein umfassendes, mehrschichtiges Audit von HTTP-Headern, Serververhalten, HTML-Strukturen und Dateien im Root-Verzeichnis durch.

#### Sicherheits- & Performance-Header-Analyse
* SSL / HTTPS-Validierung
* CSP, HSTS, Permissions-Policy, Referrer-Policy
* X-Frame-Options, X-Content-Type-Options, X-XSS-Protection
* Cache-Control, Pragma, Expires, ETag
* Gesamtprüfumfang: 227 verschiedene HTTP-Header

#### Proxy- / CDN- / WAF-Fingerprinting
* Cloudflare, Akamai, Fastly, Myra, Imperva, Sucuri
* AWS ELB, Azure Front Door, Google Cloud CDN
* Varnish, HAProxy, Traefik, OpenResty
* Stille Bot-Mitigation-Layers
* Erkennung von Reverse-Proxy-Ketten

#### Client-Hints & Bot-Schutz-Erkennung
* Accept-CH, Critical-CH
* CF-Mitigated
* Speculation-Rules & Prerendering-Erkennung (Speculation Rules API)
* Fortschrittliche Bot-Blocking-Heuristiken

#### Redirect- & Domain-Integritäts-Prüfungen
* Durchsetzung von HTTPS
* www / non-www Konsistenz
* Analyse von Weiterleitungsketten (Redirect Chains)
* Soft-404-Erkennung (mehrschichtig)

#### Consent-relevante Drittanbieter-Erkennung
*(Keine Rechtsberatung)*
* Google Fonts
* Google Tag Manager
* Microsoft Clarity
* Viele weitere Drittanbieter-Einbindungen

#### Cross-Validierung von HTML / Meta / Server
* Abgleich von HTML `<meta http-equiv>` mit echten Server-Headern
* Automatische Generierung von `.htaccess`-Regeln
* Validierung von Canonical-Tags
* Sprach- & OpenGraph-Prüfungen

#### CMS- / Shop-System-Fingerprinting (100+ Systeme)
* WordPress, Joomla, Drupal, TYPO3
* Magento, Shopware, PrestaShop, Shopify
* Ghost, Next.js, Nuxt, Express
* Laravel, Symfony, Django, Flask
* Obscurity-Check auf Server-Leaks

#### Diagnostik von Dateien im Root-Verzeichnis
* `robots.txt`
* `llms.txt`
* `llms-fulltext.txt`
* `security.txt`
* `infophp.php`
* Mehrere Index-Root-Dateien (`.php`, `.html`, `.htm`)

#### Isolations- & Obfuskations-Analyse (Quarantäne-Engine)
* Zero-Regex-Engine
* Score-basierte Erkennung von Verschleierung (Obfuskation), Loadern und versteckten Payloads
* Sicheres Filtern verdächtiger Code-Fragmente

#### E-Mail-Sicherheits-Validierung
* MX, SPF, DKIM, DMARC
* BIMI (kein Sicherheitsaspekt, rein informativ)

#### User-Agent-Testing
* 19 auswählbare User-Agents
* Erkennung einfacher UA-Blocking-Mechanismen

#### Kompatibilität mit Altsystemen
* Vollständig kompatibel mit PHP 4.3
* Konform mit der ScrapTrap-Framework-Policy

---

### 🚀 Besondere Engine-Features

#### 227-Punkt Zero-Regex-Engine
* Deterministisches Parsing
* Arbeitsspeichersicher (Memory-safe)
* Kein Catastrophic Backtracking
* Schnelle Script-Ausführung (Gesamtzeit abhängig von Serverantworten)
* Ideal für fehlerhafte oder manipulierte Eingaben (Adversarial Input)

#### Kontextsensitive Risikomatrix
Die Schweregrad-Einstufung kann den jeweiligen Seitentyp-Tooltipps entnommen werden:
* NGO / Sensibles Thema
* E-Commerce
* Blog / Magazin
* Private Webseite
* API / Headless

#### Soft-404-Falle (Entrapment)
Erkennt Server, die HTML-Fehlerseiten mit dem HTTP-Statuscode `200 OK` ausliefern.

#### Validierung von Crawler-Anweisungen
Überprüft:
* `robots.txt`
* `llms.txt`
* `llms-fulltext.txt`
* `infophp.php`
* `security.txt`

#### Infrastruktur-Fingerprinting
Entlarvt:
* WAFs
* CDNs
* Reverse Proxies
* Load Balancer
* Bot-Mitigation-Layers

---

### 🏛️ Architektonische Garantien (Privacy-First by Design)

ScrapTrap folgt einer strengen Privacy-First-Architektur ohne Datenspeicherung, entwickelt für maximale Transparenz, minimale Angriffsfläche und vollständige Unabhängigkeit von externen Diensten.

* **Keine Datenbank:** Es werden keine auditierten Daten gespeichert, protokolliert, persistiert oder auf die Festplatte geschrieben. Alle Audits laufen vollständig im Arbeitsspeicher (In-Memory) und werden sofort verworfen.
* **Keine Cloud-Abhängigkeiten:** Keine externen APIs, Cloud-Dienste oder Telemetrie-Endpunkte. Die Engine arbeitet vollständig auf dem ScrapTrap-Server ohne Drittanbieter-Aufrufe.
* **Keine JavaScript-Ausführung:** ScrapTrap führt clientseitig kein JavaScript aus. Dies verhindert skriptbasiertes Fingerprinting, Tracking oder unerwünschte Nebeneffekte.
* **Kein Tracking:** Keine Analysen, Cookies, Verhaltensprofilierung oder Nutzeridentifikation. ScrapTrap verfolgt weder Domains noch Nutzungsmuster oder den Audit-Verlauf.
* **Keine Telemetrie:** Keine Metriken, keine Nutzungsberichte, kein externes Monitoring. Das System ist für Dritte vollkommen undurchsichtig (opaque).
* **Keine Werbung:** Keine Banner, keine Affiliate-Links, keine kommerziellen Einbindungen. ScrapTrap ist ein reines Diagnose- und Didaktik-Werkzeug.
* **Keine Exploit-Ausführung:** ScrapTrap führt niemals Penetrationstests, Brute-Force-Versuche oder CVE-Exploitations durch. Es handelt sich um eine reine Read-Only-Diagnose-Engine.

---

### 📊 Laufendes empirisches Projekt: Sicherheitsdefizite in High-Risk-NGO-Infrastrukturen

Dieses Framework wird aktiv als primäres Diagnoseinstrument für eine fortlaufende empirische Sicherheitsstudie eingesetzt. Das Projekt untersucht die grundlegende technische Web-Sicherheit von öffentlich zugänglichen Webseiten in hochsensiblen Non-Profit-Bereichen (spezifischer Fokus auf **Frauenhäuser**, **Krisenberatungsstellen** und **Aidshilfe-Organisationen**).

*   **Die Dringlichkeit:** Organisationen in diesen Feldern verarbeiten hochkritische Informationen. Technische Fehlkonfigurationen oder informative Server-Leaks können hier im schlimmsten Fall direkt die physische Sicherheit und die Identität schutzbedürftiger Menschen gefährden.
*   **Bisherige Forschungsergebnisse:** Die über diese Diagnose-Engine erhobenen Daten zeichnen ein erschreckendes Bild eklatanter struktureller Mängel im NGO-Sektor. Zu den häufigsten Mustern gehören das fast vollständige Fehlen wirksamer Content Security Policies (CSP), unzureichender Schutz gegen Clickjacking (X-Frame-Options) sowie informative Server-Header, die potenziellen Angreifern die genaue Patch-Ebene der Systeme verraten.
*   **Anonymisierungsstrategie:** Um die ohnehin gefährdeten Einrichtungen keiner zusätzlichen Gefahr auszusetzen, werden alle im Rahmen der Studie erhobenen Fehlerklassen und statistischen Verteilungen vollständig anonymisiert und ohne jegliche Identifikationsmerkmale wissenschaftlich ausgewertet.


---

### 🌐 Live-Zugang

🔗 [https://scraptrap.de/scraptrap_http_header_audit.php](https://scraptrap.de/scraptrap_http_header_audit.php)

---

### ⚠️ Hinweis zum geistigen Eigentum (Intellectual Property)

Die zugrundeliegende Parser-Logik, die Heuristiken und die Diagnose-Engine sind proprietäre Komponenten des ScrapTrap Bot Mitigation & WAF Frameworks.  
Dieses Repository stellt Dokumentation, Forschungskontext und didaktisches Material bereit, nicht jedoch den Quellcode.
