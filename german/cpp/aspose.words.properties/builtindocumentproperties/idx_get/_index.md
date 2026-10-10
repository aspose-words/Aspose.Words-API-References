---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get Methode"
linktitle: "idx_get"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get Methode. Gibt ein DocumentProperty-Objekt anhand des Namens der Eigenschaft zurück in C++."
type: docs
weight: 35000
url: /de/cpp/aspose.words.properties/builtindocumentproperties/idx_get/
---
## BuiltInDocumentProperties::idx_get method


Gibt ein [DocumentProperty](../../documentproperty/) Objekt anhand des Namens der Eigenschaft zurück.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::BuiltInDocumentProperties::idx_get(System::String name) override
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | System::String | Der nicht‑groß-/kleinschreibungsabhängige Name der abzurufenden Eigenschaft. |
## Hinweise


Die Zeichenkettennamen der Eigenschaften entsprechen den Namen der typisierten Eigenschaften, die von [BuiltInDocumentProperties](../) verfügbar sind.

Wenn Sie eine Eigenschaft anfordern, die im Dokument nicht vorhanden ist, deren Name jedoch als gültiger integrierter Name erkannt wird, wird ein neues [DocumentProperty](../../documentproperty/) erstellt, zur Sammlung hinzugefügt und zurückgegeben. Die neu erstellte Eigenschaft erhält einen Standardwert (leere Zeichenkette, Null, **false** oder DateTime.MinValue, abhängig vom Typ der integrierten Eigenschaft).

Wenn Sie eine Eigenschaft anfordern, die im Dokument nicht vorhanden ist und deren Name nicht als integrierter Name erkannt wird, wird ein **null** zurückgegeben.

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
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
