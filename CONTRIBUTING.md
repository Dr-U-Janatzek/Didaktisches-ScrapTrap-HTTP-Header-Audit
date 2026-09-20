\# Contributing Guidelines – ScrapTrap Audit Framework



\[ 🇬🇧 English ](#english) | \[ 🇩🇪 Deutsch ](#deutsch)



\---



<a name="english"></a>

\## 🇬🇧 English Guidelines



Thank you for your interest in the ScrapTrap HTTP Header \& Web Security Audit project. To maintain the scientific integrity of our research and the performance stability of our diagnostic engine, we enforce strict communication guidelines.



\### 🚫 Code Contributions (Pull Requests)

\* \*\*Proprietary Software:\*\* The core parsing engine, heuristics, and source code of ScrapTrap are closed-source and proprietary intellectual property. 

\* \*\*No Pull Requests:\*\* We do not accept code contributions, patches, or pull requests. Any open pull requests containing code modifications will be closed without review.



\### 🐛 Reporting Engine Bugs \& Edge Cases

If you utilize our live tool at `scraptrap.de` and detect an architectural misinterpretation, a false-positive in the risk matrix, or an unhandled HTTP header edge case, we welcome structured bug reports via GitHub Issues.



To submit a valid report, please provide:

1\. \*\*The Target Configuration:\*\* The raw, sanitized HTTP response header string that caused the issue (ensure all tracking tokens or internal IPs are removed).

2\. \*\*The Expected Behavior:\*\* A reference to the official RFC or standard protocol detailing how the header should be parsed.

3\. \*\*The Engine Output:\*\* The specific line or error message returned by our audit script.



\### 📊 Scientific Cooperation \& NGO Data Exchange

If you are an IT security researcher, system administrator, or a representative operating within high-risk NGO environments (e.g., women's shelters, crisis intervention counseling, health support networks) and wish to contribute to our ongoing empirical study:



\* \*\*Strict Anonymization:\*\* We only accept data that has been completely stripped of domain names, branding, specific IP blocks, or any identifiers that could compromise vulnerable infrastructure or human safety.

\* \*\*Data Format:\*\* Please categorize submission vectors by error classes (e.g., "Missing CSP on informational forms", "Server-Header patch-level leaks").

\* \*\*Contact:\*\* Reach out via the communication channels specified in the main profile to coordinate secure, encrypted data sharing.



\---



<a name="deutsch"></a>

\## 🇩🇪 Deutsche Richtlinien



Vielen Dank für Ihr Interesse am ScrapTrap HTTP-Header \& Web-Security-Audit-Projekt. Um die wissenschaftliche Integrität der Forschung und die Stabilität der Diagnose-Engine zu gewährleisten, gelten für dieses Repository strukturierte Kommunikationsregeln.



\### 🚫 Code-Beiträge (Pull Requests)

\* \*\*Proprietäre Software:\*\* Die zugrundeliegende Parser-Logik, die Heuristiken und der Quellcode von ScrapTrap sind closed-source und geschütztes geistiges Eigentum.

\* \*\*Keine Pull Requests:\*\* Es werden keine Code-Zusendungen, Patches oder Pull Requests akzeptiert. Offene Pull Requests, die Code-Modifikationen enthalten, werden ungelesen geschlossen.



\### 🐛 Melden von Fehlern \& Grenzfällen (Engine Bugs)

Wenn Sie das Live-Tool auf `scraptrap.de` nutzen und eine architektonische Fehlinterpretation, ein "False-Positive" in der Risikomatrix oder einen nicht berücksichtigten HTTP-Header-Grenzfall entdecken, können Sie dies über ein strukturiertes GitHub-Issue melden.



Ein valider Fehlerbericht erfordert:

1\. \*\*Die Zielkonfiguration:\*\* Den rohen, bereinigten HTTP-Response-Header-String, der den Fehler verursacht hat (bitte interne IPs oder Tracking-Tokens vorab entfernen).

2\. \*\*Das Soll-Verhalten:\*\* Einen Verweis auf den offiziellen RFC oder Protokollstandard, der definiert, wie der Header korrekt zu parsen ist.

3\. \*\*Die Engine-Ausgabe:\*\* Den spezifischen Fehlertext oder die falsche Bewertung des Audit-Skripts.



\### 📊 Wissenschaftliche Kooperation \& NGO-Datenaustausch

Wenn Sie als IT-Sicherheitsforscher:in, Systemadministrator:innen oder Vertreter:in in einem hochsensiblen NGO-Umfeld tätig sind (z. B. Frauenhäuser, Krisenberatungsstellen, Aidshilfe-Netzwerke) und Daten zu der empirischen Sicherheitsstudie beisteuern möchten:



\* \*\*Strikte Anonymisierung:\*\* Es werden ausschließlich Datensätze, die vollständig von Domainnamen, Markenbezeichnungen, spezifischen IP-Blöcken oder jeglichen Merkmalen bereinigt wurden, die schutzbedürftige Infrastrukturen oder Menschen gefährden könnten, akzeptiert.

\* \*\*Datenformat:\*\* Bitte strukturieren Sie Einreichungen nach rein technischen Fehlerklassen (z. B. "Fehlende CSP bei Formularen", "Informative Server-Header mit Patch-Level-Leaks").

\* \*\*Kontakt:\*\* Nutzen Sie die im Hauptprofil angegebenen Kommunikationskanäle, um eine verschlüsselte Datenübermittlung zu koordinieren.



