---
title: "Aspose::Words::Properties::DocumentProperty::ToBool-Methode"
linktitle: "ToBool"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::DocumentProperty::ToBool-Methode. Gibt den Eigenschaftswert als bool in C++ zurück."
type: docs
weight: 10000
url: /de/cpp/aspose.words.properties/documentproperty/tobool/
---
## DocumentProperty::ToBool method


Gibt den Eigenschaftswert als bool zurück.

```cpp
bool Aspose::Words::Properties::DocumentProperty::ToBool()
```

## Hinweise


Wirft eine Ausnahme, wenn der Eigenschaftstyp nicht [Boolean](../../propertytype/) ist.

## Beispiele



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
