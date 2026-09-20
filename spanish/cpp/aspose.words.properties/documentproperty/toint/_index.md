---
title: "Método Aspose::Words::Properties::DocumentProperty::ToInt"
linktitle: "ToInt"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Properties::DocumentProperty::ToInt. Devuelve el valor de la propiedad como entero en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.properties/documentproperty/toint/
---
## DocumentProperty::ToInt method


Devuelve el valor de la propiedad como integer.

```cpp
int32_t Aspose::Words::Properties::DocumentProperty::ToInt()
```


## Ejemplos



Muestra varios métodos de conversión de tipo de propiedades de documento personalizadas.
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

## Ver también

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
