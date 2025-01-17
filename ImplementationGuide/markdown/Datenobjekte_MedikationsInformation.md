## MedikationsInformation [(MedicationStatement)](https://www.hl7.org/fhir/medicationstatement.html)

---

### Profil

@```
from StructureDefinition where url = 'https://gematik.de/fhir/isik/v3/Medikation/StructureDefinition/ISiKMedikationsInformation' select Name: name, Canonical: url
```

{{tree:https://gematik.de/fhir/isik/v3/Medikation/StructureDefinition/ISiKMedikationsInformation, hybrid}}

---

**Terminology Bindings**

@```
from StructureDefinition
where url in ('https://gematik.de/fhir/isik/v3/Medikation/StructureDefinition/ISiKMedikationsInformation' )
for differential.element
select
Path: path,
join binding.where(valueSet.exists())
{
  Name: valueSet.substring((9 + valueSet.indexOf('ValueSet/'))),
  Strength: strength,
  URL: valueSet
}
```

---

### Anmerkungen zu Must-Support-Feldern

@```from
	StructureDefinition
where
    url = 'https://gematik.de/fhir/isik/v3/Medikation/StructureDefinition/ISiKMedikationsInformation'
for differential.element
where mustSupport = true
  and short.exists()
select
	Feldname: id, Kurzbeschreibung: short, Hinweise: comment
```

## Beispiele

Valide Beispiele für das Profil MedikationsInformation:

{{json:ExampleISiKMedikationsInformation1}}

{{json:ExampleISiKMedikationsInformation2}}

## Interaktionen

Für die Ressource MedicationStatement MÜSSEN die REST-Interaktionen "READ", "CREATE" und "UPDATE" implementiert werden.

Folgende Suchparameter sind für das Bestätigungsverfahren relevant, auch in Kombination:

1. Der Suchparameter "_id" MUSS unterstützt werden:

    Beispiele:

    ```GET [base]/MedicationStatement?_id=103270```

    Anwendungshinweise: Weitere Informationen zur Suche nach "_id" finden sich in der [FHIR-Basisspezifikation - Abschnitt "Parameters for all resources"](http://hl7.org/fhir/R4/search.html#all).

1. Der Suchparameter "code" MUSS unterstützt werden:

    Beispiele:

    ```GET [base]/MedicationStatement.code=http://fhir.de/CodeSystem/bfarm/atc|V03AB23```

    Anwendungshinweise: Weitere Informationen zur Suche nach Token-type Parametern finden sich in der [FHIR-Basisspezifikation - Abschnitt "Token Search"](http://hl7.org/fhir/R4/search.html#token).

1. Der Suchparameter "context" MUSS unterstützt werden:

   Beispiele:

    ```GET [base]/MedicationStatement?context=Encounter/123```

    Anwendungshinweise: Weitere Informationen zur Suche nach Reference-type Parametern finden sich in der [FHIR-Basisspezifikation - Abschnitt "Reference Search"](https://www.hl7.org/fhir/search.html#reference).

1. Der verkettete Suchparameter "context.identifier" MUSS unterstützt werden:

   Beispiele:

   ```GET [base]/MedicationStatement?context.identifier=http://mein-krankenhaus.example/fhir/sid/fallnummern|7567867```

	 ```GET [base]/MedicationStatement?context.identifier=7567867```

   Anwendungshinweise: Weitere Informationen zur Suche nach Reference-type Parametern finden sich in der [FHIR-Basisspezifikation - Abschnitt "Reference Search"](https://www.hl7.org/fhir/search.html#reference).

	 Weitere Informationen zur Suche nach verketteten Parametern finden sich in der [FHIR-Basisspezifikation - Abschnitt "Chained Parameters"](http://hl7.org/fhir/search.html#chaining).

1. Der Suchparameter "effective" MUSS unterstützt werden:

    Beispiele:

    ```GET [base]/MedicationStatement.effective=2022-03-21```

    Anwendungshinweise: Weitere Informationen zur Suche nach Date-type Parametern finden sich in der [FHIR-Basisspezifikation - Abschnitt "Date"](http://hl7.org/fhir/R4/search.html#date).

1. Der Suchparameter "medication" MUSS unterstützt werden:

   Beispiele:

    ```GET [base]/MedicationStatement?medication=Medication/123```

    Anwendungshinweise: Weitere Informationen zur Suche nach Reference-type Parametern finden sich in der [FHIR-Basisspezifikation - Abschnitt "Reference Search"](https://www.hl7.org/fhir/search.html#reference).

1. Der verkettete Suchparameter "medication.code" MUSS unterstützt werden:

    Beispiele:

    ```GET [base]/MedicationStatement?medication.code=http://fhir.de/CodeSystem/bfarm/atc|V03AB23```

    Anwendungshinweise: Weitere Informationen zur Suche nach Token-type Parametern finden sich in der [FHIR-Basisspezifikation - Abschnitt "Token Search"](http://hl7.org/fhir/R4/search.html#token).

	  Weitere Informationen zur Suche nach verketteten Parametern finden sich in der [FHIR-Basisspezifikation - Abschnitt "Chained Parameters"](http://hl7.org/fhir/search.html#chaining).

1. Der Suchparameter "part-of" MUSS unterstützt werden:

   Beispiele:

    ```GET [base]/MedicationStatement?part-of=MedicationAdministration/789```

    Anwendungshinweise: Weitere Informationen zur Suche nach Reference-type Parametern finden sich in der [FHIR-Basisspezifikation - Abschnitt "Reference Search"](https://www.hl7.org/fhir/search.html#reference).

1. Der Suchparameter "patient" MUSS unterstützt werden:

   Beispiele:

    ```GET [base]/MedicationStatement?patient=Patient/123```

    Anwendungshinweise: Weitere Informationen zur Suche nach Reference-type Parametern finden sich in der [FHIR-Basisspezifikation - Abschnitt "Reference Search"](https://www.hl7.org/fhir/search.html#reference).

1. Der verkettete Suchparameter "patient.identifier" MUSS unterstützt werden:

    Beispiele:

    ```GET [base]/MedicationStatement?patient.identifier=http://mein-krankenhaus.example/fhir/sid/patienten|1032702```

    ```GET [base]/MedicationStatement?patient.identifier=1032702```

    Anwendungshinweise: Weitere Informationen zur Suche nach Token-type Parametern finden sich in der [FHIR-Basisspezifikation - Abschnitt "Token Search"](http://hl7.org/fhir/R4/search.html#token).

	Weitere Informationen zur Suche nach verketteten Parametern finden sich in der [FHIR-Basisspezifikation - Abschnitt "Chained Parameters"](http://hl7.org/fhir/search.html#chaining).

1. Der Suchparameter "status" MUSS unterstützt werden:

    Beispiele:

    ```GET [base]/MedicationStatement.status=active```

    Anwendungshinweise: Weitere Informationen zur Suche nach Token-type Parametern finden sich in der [FHIR-Basisspezifikation - Abschnitt "Token Search"](http://hl7.org/fhir/R4/search.html#token).
