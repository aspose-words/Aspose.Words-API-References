---
title: "Aspose::Words::Markup::CustomXmlPropertyCollection clase"
linktitle: "CustomXmlPropertyCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::CustomXmlPropertyCollection clase. Representa una colección de atributos XML personalizados o propiedades de etiquetas inteligentes. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class


Representa una colección de atributos XML personalizados o propiedades de etiqueta inteligente. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlProperty\>\&) | Agrega una propiedad a la colección. |
| [Clear](./clear/)() | Elimina todos los elementos de la colección. |
| [Contains](./contains/)(const System::String\&) | Determina si la colección contiene una propiedad con el nombre dado. |
| [get_Count](./get_count/)() | Obtiene el número de elementos contenidos en la colección. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador que puede usarse para iterar sobre todos los elementos de la colección. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Obtiene una propiedad con el nombre especificado. |
| [idx_get](./idx_get/)(int32_t) | Obtiene una propiedad en el índice especificado. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Devuelve el índice basado en cero de la propiedad especificada en la colección. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Elimina una propiedad con el nombre especificado de la colección. |
| [RemoveAt](./removeat/)(int32_t) | Elimina una propiedad en el índice especificado. |
| static [Type](./type/)() |  |
## Observaciones


Los elementos son objetos [CustomXmlProperty](../customxmlproperty/).

## Ejemplos



Muestra cómo trabajar con las propiedades de etiquetas inteligentes para obtener información detallada sobre las etiquetas inteligentes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

// Una etiqueta inteligente aparece en un documento cuando Microsoft Word reconoce una parte de su texto como algún tipo de dato,
// como un nombre, una fecha o una dirección, y la convierte en un hipervínculo que muestra un subrayado punteado púrpura.
// En Word 2003, podemos habilitar las etiquetas inteligentes a través de "Herramientas" -> "Opciones de autocorrección..." -> "SmartTags".
// En nuestro documento de entrada, hay tres objetos que Microsoft Word registró como etiquetas inteligentes.
// Las etiquetas inteligentes pueden estar anidadas, por lo que esta colección contiene más.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Markup::SmartTag>> smartTags = doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::SmartTag> >()->LINQ_ToArray();

ASSERT_EQ(8, smartTags->get_Length());

// El miembro "Properties" de una etiqueta inteligente contiene sus metadatos, que serán diferentes para cada tipo de etiqueta inteligente.
// Las propiedades de una etiqueta inteligente de tipo "date" contienen su año, mes y día.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPropertyCollection> properties = smartTags[7]->get_Properties();

ASSERT_EQ(4, properties->get_Count());

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Property name: {0}, value: {1}", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Value()) << std::endl;
        ASSERT_EQ(u"", enumerator->get_Current()->get_Uri());
    }
}

// También podemos acceder a las propiedades de varias maneras, como un par clave-valor.
ASSERT_TRUE(properties->Contains(u"Day"));
ASSERT_EQ(u"22", properties->idx_get(u"Day")->get_Value());
ASSERT_EQ(u"2003", properties->idx_get(2)->get_Value());
ASSERT_EQ(1, properties->IndexOfKey(u"Month"));

// A continuación se presentan tres formas de eliminar elementos de la colección de propiedades.
// 1 -  Eliminar por índice:
properties->RemoveAt(3);

ASSERT_EQ(3, properties->get_Count());

// 2 -  Eliminar por nombre:
properties->Remove(u"Year");

ASSERT_EQ(2, properties->get_Count());

// 3 -  Vacía la colección completa de una vez:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Ver también

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
