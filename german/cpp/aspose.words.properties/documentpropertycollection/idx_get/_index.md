---
title: "Aspose::Words::Properties::DocumentPropertyCollection::idx_get Methode"
linktitle: "idx_get"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::DocumentPropertyCollection::idx_get Methode. Gibt ein DocumentProperty-Objekt nach Index in C++ zurück."
type: docs
weight: 7000
url: /de/cpp/aspose.words.properties/documentpropertycollection/idx_get/
---
## DocumentPropertyCollection::idx_get(int32_t) method


Gibt ein [DocumentProperty](../../documentproperty/) Objekt nach Index zurück.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(int32_t index)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Nullbasierter Index des zu holenden [DocumentProperty](../../documentproperty/). |

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

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentPropertyCollection::idx_get(System::String) method


Gibt ein [DocumentProperty](../../documentproperty/) Objekt anhand des Namens der Eigenschaft zurück.

```cpp
virtual System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(System::String name)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | System::String | Der nicht‑groß-/kleinschreibungsabhängige Name der abzurufenden Eigenschaft. |
## Hinweise


Gibt **null** zurück, wenn eine Eigenschaft mit dem angegebenen Namen nicht gefunden wird.

## Beispiele



Zeigt, wie man eine benutzerdefinierte Dokumenteigenschaft erstellt, die ein Datum und eine Uhrzeit enthält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```

## Siehe auch

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
