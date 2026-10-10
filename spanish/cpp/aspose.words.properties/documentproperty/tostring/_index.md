---
title: "Aspose::Words::Properties::DocumentProperty::ToString método"
linktitle: "ToString"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::DocumentProperty::ToString método. Devuelve el valor de la propiedad como una cadena formateada según la configuración regional actual en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty::ToString method


Devuelve el valor de la propiedad como una cadena formateada según la configuración regional actual.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::ToString() const override
```

## Observaciones


Convierte una propiedad booleana en "Y" o "N". Convierte una propiedad de fecha en una cadena de fecha corta. Para todos los demás tipos, convierte una propiedad usando Object.ToString().

## Ejemplos



Muestra cómo trabajar con propiedades de documento personalizadas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Cada documento contiene una colección de propiedades personalizadas, que, al igual que las propiedades incorporadas, son pares clave-valor.
// El documento tiene una lista fija de propiedades incorporadas. El usuario crea todas las propiedades personalizadas.
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
