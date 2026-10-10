---
title: "Aspose::Words::Properties::DocumentProperty::ToDateTime metodo"
linktitle: "ToDateTime"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::DocumentProperty::ToDateTime metodo. Restituisce il valore della proprietà come DateTime in UTC in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty::ToDateTime method


Restituisce il valore della proprietà come **DateTime** in UTC.

```cpp
System::DateTime Aspose::Words::Properties::DocumentProperty::ToDateTime()
```

## Note


Lancia un'eccezione se il tipo della proprietà non è [DateTime](../../propertytype/).

Microsoft Word memorizza solo la parte data (senza ora) per le proprietà data personalizzate.

## Esempi



Mostra come creare una proprietà documento personalizzata che contiene data e ora.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```


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
