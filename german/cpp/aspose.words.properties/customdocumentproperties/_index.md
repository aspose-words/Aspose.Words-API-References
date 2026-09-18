---
title: "Aspose::Words::Properties::CustomDocumentProperties Klasse"
linktitle: "CustomDocumentProperties"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::CustomDocumentProperties Klasse. Eine Sammlung von benutzerdefinierten Dokumenteigenschaften. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class


Eine Sammlung benutzerdefinierter Dokumenteigenschaften. Weitere Informationen finden Sie im Dokumentationsartikel [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class CustomDocumentProperties : public Aspose::Words::Properties::DocumentPropertyCollection
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft vom Datentyp [String](../propertytype/). |
| [Add](./add/)(const System::String\&, int32_t) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft vom Datentyp [Number](../propertytype/). |
| [Add](./add/)(const System::String\&, System::DateTime) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft vom Datentyp [DateTime](../propertytype/). |
| [Add](./add/)(const System::String\&, bool) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft vom Datentyp [Boolean](../propertytype/). |
| [Add](./add/)(const System::String\&, double) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft vom Datentyp [Double](../propertytype/). |
| [AddLinkToContent](./addlinktocontent/)(const System::String\&, const System::String\&) | Erstellt eine neue, mit Inhalt verknüpfte benutzerdefinierte Dokumenteigenschaft. |
| [Clear](../documentpropertycollection/clear/)() | Entfernt alle Eigenschaften aus der Sammlung. |
| [Contains](../documentpropertycollection/contains/)(const System::String\&) | Gibt **true** zurück, wenn eine Eigenschaft mit dem angegebenen Namen in der Sammlung existiert. |
| [get_Count](../documentpropertycollection/get_count/)() | Ermittelt die Anzahl der Elemente in der Sammlung. |
| [GetEnumerator](../documentpropertycollection/getenumerator/)() override | Gibt ein Enumerator‑Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](../documentpropertycollection/idx_get/)(System::String) | Gibt ein [DocumentProperty](../documentproperty/)-Objekt anhand des Namens der Eigenschaft zurück. |
| [idx_get](../documentpropertycollection/idx_get/)(int32_t) | Gibt ein [DocumentProperty](../documentproperty/)-Objekt anhand des Index zurück. |
| [IndexOf](../documentpropertycollection/indexof/)(const System::String\&) | Ermittelt den Index einer Eigenschaft anhand ihres Namens. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../documentpropertycollection/remove/)(const System::String\&) | Entfernt eine Eigenschaft mit dem angegebenen Namen aus der Sammlung. |
| [RemoveAt](../documentpropertycollection/removeat/)(int32_t) | Entfernt eine Eigenschaft am angegebenen Index. |
| static [Type](./type/)() |  |
## Hinweise


Jedes [DocumentProperty](../documentproperty/)-Objekt stellt eine benutzerdefinierte Eigenschaft eines Containerdokuments dar.

Die Namen der Eigenschaften sind nicht zwischen Groß- und Kleinschreibung unterscheidend.

Die Eigenschaften in der Sammlung werden alphabetisch nach Namen sortiert.

## Beispiele



Zeigt, wie man mit benutzerdefinierten Dokumenteigenschaften arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Jedes Dokument enthält eine Sammlung benutzerdefinierter Eigenschaften, die, wie die integrierten Eigenschaften, Schlüssel-Wert-Paare sind.
// Das Dokument hat eine feste Liste integrierter Eigenschaften. Der Benutzer erstellt alle benutzerdefinierten Eigenschaften.
ASSERT_EQ(u"Value of custom document property", System::ObjectExt::ToString(doc->get_CustomDocumentProperties()->idx_get(u"CustomProperty")));

doc->get_CustomDocumentProperties()->Add(u"CustomProperty2", System::String(u"Value of custom document property #2"));

std::cout << "Custom Properties:" << std::endl;
for (auto&& customDocumentProperty : System::IterateOver(doc->get_CustomDocumentProperties()))
{
    std::cout << customDocumentProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", customDocumentProperty->get_Type()) << std::endl;
    std::cout << System::String::Format(u"\tValue:\t\"{0}\"", customDocumentProperty->get_Value()) << std::endl;
}
```

## Siehe auch

* Class [DocumentPropertyCollection](../documentpropertycollection/)
* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
