---
title: "Aspose::Words::Properties::DocumentProperty::ToBool metodo"
linktitle: "ToBool"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::DocumentProperty::ToBool metodo. Restituisce il valore della proprietà come booleano in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.properties/documentproperty/tobool/
---
## DocumentProperty::ToBool method


Restituisce il valore della proprietà come bool.

```cpp
bool Aspose::Words::Properties::DocumentProperty::ToBool()
```

## Note


Genera un'eccezione se il tipo della proprietà non è [Boolean](../../propertytype/).

## Esempi



Mostra vari metodi di conversione di tipo delle proprietà di documento personalizzate.
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

## Vedi anche

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
