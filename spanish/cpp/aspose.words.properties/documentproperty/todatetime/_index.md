---
title: "Aspose::Words::Properties::DocumentProperty::ToDateTime método"
linktitle: "ToDateTime"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::DocumentProperty::ToDateTime método. Devuelve el valor de la propiedad como DateTime en UTC en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty::ToDateTime method


Devuelve el valor de la propiedad como **DateTime** en UTC.

```cpp
System::DateTime Aspose::Words::Properties::DocumentProperty::ToDateTime()
```

## Observaciones


Lanza una excepción si el tipo de la propiedad no es [DateTime](../../propertytype/).

Microsoft Word almacena solo la parte de fecha (sin hora) para propiedades de fecha personalizadas.

## Ejemplos



Muestra cómo crear una propiedad de documento personalizada que contiene una fecha y hora.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```


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
