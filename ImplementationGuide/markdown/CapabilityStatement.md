## Konformitätserklärung [(CapabilityStatement)](http://hl7.org/fhir/capabilitystatement.html)

Jede Instanz eines bestätigungsrelevanten Systems MUSS an ihrem Endpunkt eine [CapabilityStatement](http://hl7.org/fhir/capabilitystatement.html)-Ressource bereitstellen.

Hierzu MUSS die [capabilities-Interaktion gemäß FHIR-Spezifikation](http://hl7.org/fhir/http.html#capabilities) unterstützt werden.
Der MODE-Parameter kann ignoriert werden.

Die CapabilityStatements in dieser Spezifikation stellen die Anforderungen seitens der gematik für den jeweiligen Bereich dieser Spezifikation dar. (`kind` = "requirements"). Zur Unterscheidung von Anforderungen, die erfüllt werden MÜSSEN gegenüber jenen, die erfüllt werden KÖNNEN, wird die [CapabilityStatement-Expectation](http://hl7.org/fhir/extension-capabilitystatement-expectation.html)-Extension mit den möglichen Werten "SHALL" (=MUSS) und "MAY" (=KANN) verwendet.

Eine Server-Instanz MUSS ihrerseits ein CapabilityStatement vom `kind`= "instance" liefern und im Element `software` den Namen und die Versionsnummer angeben.

Darüber hinaus MUSS in 'CapabilityStatement.instantiates' die Canonical URL des nachfolgenden CapabilityStatement in der jeweiligen CapabilityStatement Instanz angegeben werden.

Das CapabilityStatement der Instanz MUSS alle Funktionalitäten auflisten, die in dem folgenden, für den zu bestätigenden Bereich relevanten, CapabilityStatement mit "SHALL" gekennzeichnet sind. Das CapabilityStatement KANN darüber hinaus die mit "MAY" gekennzeichneten Funktionalitäten, sowie weitere Funktionalitäten auflisten, sofern diese in der Instanz implementiert wurden.

Implementiert ein System mehr als einen der drei Bereiche dieser Spezifikation, so MUSS dessen CapabilityStatement die Vereinigung der Funktionalitäten der betreffenden CapabilityStatements dieses Implementierungsleitfadens enthalten. Bei gleichartigen Elementen mit unterschiedlicher Anforderungsstärke (expectation) MUSS die stärkere Anforderung umgesetzt werden ("SHALL" gilt vor "MAY"). Ebenso MÜSSEN in diesem Fall die Canonical URLs der CapabilityStatements aller unten genannter implementierter Bereiche in 'CapabilityStatement.instantiates' angegeben werden.

Die Verwendung der [CapabilityStatement-Expectation](http://hl7.org/fhir/extension-capabilitystatement-expectation.html)-Extension ist im CapabilityStatement der Server-Instanz nicht erforderlich.

Die für dieses Modul bestätigungsrelevanten Teile des [Moduls "Basis"](https://simplifier.net/guide/implementierungsleitfadenisik-basismodul/ImplementationGuide-markdown-Einfuehrung?version=current) sind in den CapabilityStatements ebenfalls enthalten.


### CapabilityStatement (Requirement) ISiK-Medikation - Bereich Medikationsinformation

Canonical: https://gematik.de/fhir/isik/v3/Medikation/CapabilityStatement/medikation-server/information

{{render:https://gematik.de/fhir/isik/v3/Medikation/CapabilityStatement/medikation-server/information}}

### CapabilityStatement (Requirement) ISiK-Medikation - Bereich Medikationsverordnung

Canonical: https://gematik.de/fhir/isik/v3/Medikation/CapabilityStatement/medikation-server/verordnung

{{render:https://gematik.de/fhir/isik/v3/Medikation/CapabilityStatement/medikation-server/verordnung}}

### CapabilityStatement (Requirement) ISiK-Medikation - Bereich Medikationsverabreichung

Canonical: https://gematik.de/fhir/isik/v3/Medikation/CapabilityStatement/medikation-server/verabreichung

{{render:https://gematik.de/fhir/isik/v3/Medikation/CapabilityStatement/medikation-server/verabreichung}}
