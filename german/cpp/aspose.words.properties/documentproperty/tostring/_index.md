---
title: "Aspose::Words::Properties::DocumentProperty::ToString-Methode"
linktitle: "ToString"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::DocumentProperty::ToString-Methode. Gibt den Eigenschaftswert als Zeichenkette zurück, die gemäß dem aktuellen Gebietsschema in C++ formatiert ist."
type: docs
weight: 15000
url: /de/cpp/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty::ToString method


Gibt den Eigenschaftswert als Zeichenkette zurück, die gemäß dem aktuellen Gebietsschema formatiert ist.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::ToString() const override
```

## Hinweise


Konvertiert eine boolesche Eigenschaft in "Y" oder "N". Konvertiert eine Datumseigenschaft in eine Kurzdatumszeichenkette. Für alle anderen Typen wird eine Eigenschaft mittels Object.ToString() konvertiert.

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


Zeigt verschiedene Typkonvertierungsmethoden benutzerdefinierter Dokumenteigenschaften.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

System::DateTime authDate = System::DateTime::get_Today();
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", authDate);
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

ASPOSE_ASSERT_EQ(true, properties->idx_get(u"Authorized")->ToBool());
ASSERT_EQ(u"John Doe", System::ObjectExt::ToString(properties->idx_get(u"Authorized By")));
ASSERT_EQ(authDate, properties->idx_get(u"Authorized Date")->ToDateTime());
ASSERT_EQ(1, properties->idx_get(u"Authorized Revision")->ToInt());
ASPOSE_ASSERT_EQ(123.45, properties->idx_get(u"Authorized Amount")->ToDouble());
```

## Siehe auch

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
