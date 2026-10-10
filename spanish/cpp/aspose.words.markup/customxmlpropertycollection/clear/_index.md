---
title: "Método Clear de Aspose::Words::Markup::CustomXmlPropertyCollection"
linktitle: "Clear"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Clear de Aspose::Words::Markup::CustomXmlPropertyCollection. Elimina todos los elementos de la colección en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.markup/customxmlpropertycollection/clear/
---
## CustomXmlPropertyCollection::Clear method


Elimina todos los elementos de la colección.

```cpp
void Aspose::Words::Markup::CustomXmlPropertyCollection::Clear()
```


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

* Class [CustomXmlPropertyCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
