UC1 – Neues Gesundheitsproblem oder neue Diagnose dokumentieren

### Beschreibung

Im Rahmen der Versorgung wird bei einer Patientin oder einem Patienten ein neues Gesundheitsproblem oder eine neue Diagnose festgestellt und im klinischen Informationssystem erfasst. Die Erfassung kann in verschiedenen Stadien der diagnostischen Abklärung und mit unterschiedlicher diagnostischer Sicherheit erfolgen.
image-20261025-203426.png
plantUML UC1 - document new health problem / new diagnosis

### Beispiel

Eine Patientin stellt sich mit Fieber und linksseitigen Flankenschmerzen vor. Aufgrund der initialen klinischen Beurteilung wird zunächst das noch nicht abschliessend geklärte Gesundheitsproblem «Pyelonephritis» mit der Diagnosesicherheit «Verdacht» und der Seitenangabe «Einseitig links» erfasst.

Im Rahmen der weiteren diagnostischen Abklärung wird eine akute Pyelonephritis bestätigt. Das bereits bestehende Gesundheitsproblem wird entsprechend diagnostisch präzisiert und in «Akute Pyelonephritis» umbenannt. Gleichzeitig wird die Diagnosesicherheit von «Verdacht» auf «Bestätigt» angepasst. Die bereits dokumentierte Seitenangabe «Einseitig links» bleibt unverändert bestehen. Es wird kein neues Gesundheitsproblem angelegt. Die Information wird als dasselbe Gesundheitsproblem longitudinal weitergeführt.

<div>{% include uc1sequence.svg %}</div>

Informationsanforderungen

Ein neu erfasstes Gesundheitsproblem oder eine Diagnose kann insbesondere durch folgende Informationen beschrieben und qualifiziert werden:

    klinisch gebräuchliche Bezeichnung des Gesundheitsproblems oder der Diagnose;

    terminologische Codierung und verwendetes Codesystem;

    klinische Beschreibung;

    anatomische Lokalisation und Seitenangabe;

    Erstsymptomatik (ES);

    Erstdiagnose (ED);

    diagnostische und klinische Qualifikatoren, insbesondere Diagnosesicherheit, Aktivitätsstatus, Verlaufskategorie, Schweregrad und Auftreten;

    ergänzende klinische Informationen und Kommentare.

Welche Informationen erforderlich oder sinnvoll sind, hängt vom jeweiligen Gesundheitsproblem bzw. der Diagnose und vom klinischen Kontext ab. Bei der Ersterfassung müssen noch nicht alle Informationen vorliegen. Diese können im weiteren Verlauf der diagnostischen Abklärung und Versorgung ergänzt, präzisiert oder angepasst werden.

Erwartetes Ergebnis

Das Gesundheitsproblem bzw. die Diagnose ist als eigenständige strukturierte klinische Information in der longitudinalen Krankengeschichte erfasst. Damit ist die Grundlage geschaffen, die klinische Information im weiteren Verlauf zu ergänzen, zu präzisieren oder anzupassen sowie für unterschiedliche Darstellungs-, Verknüpfungs- und Austauschprozesse zu verwenden.

Hinweis

Die für die Darstellung verwendete Bezeichnung eines Gesundheitsproblems oder einer Diagnose kann durch eine Implementierung aus mehreren strukturierten Informationen zusammengesetzt werden. Beispielsweise kann aus der Bezeichnung «Akute Pyelonephritis» und der separat dokumentierten Seitenangabe «Einseitig links» die Anzeige «Akute Pyelonephritis links» erzeugt werden. Analog kann die Diagnosesicherheit, beispielsweise «Verdacht», bei Bedarf in die angezeigte Bezeichnung einbezogen werden. Die zugrunde liegenden Informationen bleiben dabei als eigenständige strukturierte Attribute erhalten.

Anforderungen an die Implementierung

Für die Umsetzung dieses Use Cases sind insbesondere folgende Anforderungen zu berücksichtigen:

    Unabhängige Attribute: Klinische Bezeichnung, Codierung, anatomische Angaben sowie diagnostische und klinische Qualifikatoren können unabhängig voneinander erfasst und angepasst werden.

    Schrittweise Vervollständigung: Ein Gesundheitsproblem kann zunächst mit den verfügbaren Informationen erfasst und im Rahmen der weiteren diagnostischen Abklärung ergänzt oder präzisiert werden.

    Weiterführung desselben Gesundheitsproblems: Eine diagnostische Präzisierung erfolgt durch Anpassung des bereits erfassten Gesundheitsproblems und nicht durch die Anlage eines neuen Gesundheitsproblems.