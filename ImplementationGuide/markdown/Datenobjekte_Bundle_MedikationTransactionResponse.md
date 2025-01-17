## Bundle MedikationTransactionResponse [(Bundle)](https://www.hl7.org/fhir/bundle.html)

---

### Profil

@```
from StructureDefinition where url = 'https://gematik.de/fhir/isik/v3/Medikation/StructureDefinition/ISiKMedikationTransactionResponse' select Name: name, Canonical: url
```

{{tree:https://gematik.de/fhir/isik/v3/Medikation/StructureDefinition/ISiKMedikationTransactionResponse, hybrid}}

### Anmerkungen zu Must-Support-Feldern

@```from
	StructureDefinition
where
    url = 'https://gematik.de/fhir/isik/v3/Medikation/StructureDefinition/ISiKMedikationTransactionResponse'
for differential.element
where mustSupport = true
  and short.exists()
select
	Feldname: id, Kurzbeschreibung: short, Hinweise: comment
```

### Beispiele

Valides Beispiel für das Profil MedikationTransactionResponse:

{{json:ExampleISiKMedikationTransactionResponse}}

### Interaktionen

TransactionResponse-Bundles werden nicht persistiert, sondern ausschließlich im Kontext von FHIR-Transaktionen verwendet, vgl. [FHIR RESTful API - Batch/Transaction](http://www.hl7.org/fhir/http.html#transaction).
