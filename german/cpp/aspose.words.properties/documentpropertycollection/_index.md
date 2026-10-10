---
title: "Aspose::Words::Properties::DocumentPropertyCollection Klasse"
linktitle: "DocumentPropertyCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::DocumentPropertyCollection Klasse. Basisklasse für BuiltInDocumentProperties- und CustomDocumentProperties-Sammlungen. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class


Basisklasse für die Sammlungen [BuiltInDocumentProperties](../builtindocumentproperties/) und [CustomDocumentProperties](../customdocumentproperties/). Weitere Informationen finden Sie im Dokumentationsartikel [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class DocumentPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clear](./clear/)() | Entfernt alle Eigenschaften aus der Sammlung. |
| [Contains](./contains/)(const System::String\&) | Gibt **true** zurück, wenn eine Eigenschaft mit dem angegebenen Namen in der Sammlung existiert. |
| [get_Count](./get_count/)() | Ermittelt die Anzahl der Elemente in der Sammlung. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator‑Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](./idx_get/)(System::String) | Gibt ein [DocumentProperty](../documentproperty/)-Objekt anhand des Namens der Eigenschaft zurück. |
| [idx_get](./idx_get/)(int32_t) | Gibt ein [DocumentProperty](../documentproperty/)-Objekt anhand des Index zurück. |
| [IndexOf](./indexof/)(const System::String\&) | Ermittelt den Index einer Eigenschaft anhand ihres Namens. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Entfernt eine Eigenschaft mit dem angegebenen Namen aus der Sammlung. |
| [RemoveAt](./removeat/)(int32_t) | Entfernt eine Eigenschaft am angegebenen Index. |
| static [Type](./type/)() |  |
## Hinweise


Die Namen der Eigenschaften sind nicht zwischen Groß- und Kleinschreibung unterscheidend.

Die Eigenschaften in der Sammlung werden alphabetisch nach Namen sortiert.

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
