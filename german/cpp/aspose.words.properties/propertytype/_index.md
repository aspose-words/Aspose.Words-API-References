---
title: "Aspose::Words::Properties::PropertyType enum"
linktitle: "PropertyType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::PropertyType enum. Gibt den Datentyp einer Dokumenteigenschaft in C++ an."
type: docs
weight: 6000
url: /de/cpp/aspose.words.properties/propertytype/
---
## PropertyType enum


Gibt den Datentyp einer Dokumenteigenschaft an.

```cpp
enum class PropertyType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Boolean | 0 | Die Eigenschaft ist ein boolescher Wert. |
| DateTime | 1 | Die Eigenschaft ist ein Datum‑Uhrzeit‑Wert. |
| Double | 2 | Die Eigenschaft ist eine Gleitkommazahl. |
| Number | 3 | Die Eigenschaft ist eine Ganzzahl. |
| String | 4 | Die Eigenschaft ist ein Zeichenkettenwert. |
| StringArray | 5 | Die Eigenschaft ist ein Array von Zeichenketten. |
| ObjectArray | 6 | Die Eigenschaft ist ein Array von Objekten. |
| ByteArray | 7 | Die Eigenschaft ist ein Array von Bytes. |
| Andere | 8 | Die Eigenschaft ist ein anderer Typ. |


## Beispiele



Zeigt, wie man mit den benutzerdefinierten Eigenschaften eines Dokuments arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Benutzerdefinierte Dokumenteigenschaften sind Schlüssel‑Wert‑Paare, die wir dem Dokument hinzufügen können.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// Die Sammlung sortiert die benutzerdefinierten Eigenschaften alphabetisch.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Gibt jede benutzerdefinierte Eigenschaft im Dokument aus.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Zeigt den Wert einer benutzerdefinierten Eigenschaft mithilfe eines DOCPROPERTY‑Feldes an.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Wir können diese benutzerdefinierten Eigenschaften in Microsoft Word über \"Datei\" -> \"Eigenschaften\" > \"Erweiterte Eigenschaften\" > \"Benutzerdefiniert\" finden.
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Im Folgenden sind drei Möglichkeiten zum Entfernen benutzerdefinierter Eigenschaften aus einem Dokument aufgeführt.
// 1 -  Entfernen nach Index:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Entfernen nach Name:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Die gesamte Sammlung auf einmal leeren:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Siehe auch

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
