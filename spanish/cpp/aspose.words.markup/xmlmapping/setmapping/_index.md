---
title: "Método Aspose::Words::Markup::XmlMapping::SetMapping"
linktitle: "SetMapping"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Markup::XmlMapping::SetMapping. Establece una asignación entre la etiqueta de documento estructurado principal y un nodo XML de una parte de datos XML personalizada en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.markup/xmlmapping/setmapping/
---
## XmlMapping::SetMapping method


Establece una asignación entre la etiqueta de documento estructurado principal y un nodo XML de una parte de datos XML personalizada.

```cpp
bool Aspose::Words::Markup::XmlMapping::SetMapping(const System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> &customXmlPart, const System::String &xPath, const System::String &prefixMapping)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| customXmlPart | const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\& | Una parte de datos XML personalizada a la que asignar. |
| xPath | const System::String\& | Una expresión XPath para encontrar el nodo XML. |
| prefixMapping | const System::String\& | Mapeos de prefijos de espacio de nombres XML para evaluar el XPath. |

### ReturnValue

Una bandera que indica si la etiqueta de documento estructurado principal está asignada correctamente al nodo XML.

## Ejemplos



Muestra cómo crear una etiqueta de documento estructurado con datos XML personalizados.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Construya una parte XML que contenga datos y agréguela a la colección del documento.
// Si habilitamos la pestaña "Developer" en Microsoft Word,
// podemos encontrar elementos de esta colección en el "XML Mapping Pane", junto con algunos elementos predeterminados.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello world!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASPOSE_ASSERT_EQ(System::Text::Encoding::get_ASCII()->GetBytes(xmlPartContent), xmlPart->get_Data());
ASSERT_EQ(xmlPartId, xmlPart->get_Id());

// A continuación se presentan dos formas de referirse a las partes XML.
// 1 -  Por un índice en la colección de partes XML personalizadas:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->idx_get(0));

// 2 -  Por GUID:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->GetById(xmlPartId));

// Agregar una asociación de esquema XML.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Clonar una parte y luego insertarla en la colección.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPartClone = xmlPart->Clone();
xmlPartClone->set_Id(System::Guid::NewGuid().ToString(u"B"));
doc->get_CustomXmlParts()->Add(xmlPartClone);

ASSERT_EQ(2, doc->get_CustomXmlParts()->get_Count());

// Iterar a través de la colección e imprimir el contenido de cada parte.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>> enumerator = doc->get_CustomXmlParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"XML part index {0}, ID: {1}", index, enumerator->get_Current()->get_Id()) << std::endl;
        std::cout << System::String::Format(u"\tContent: {0}", System::Text::Encoding::get_UTF8()->GetString(enumerator->get_Current()->get_Data())) << std::endl;
        index++;
    }
}

// Utilice el método "RemoveAt" para eliminar la parte clonada por índice.
doc->get_CustomXmlParts()->RemoveAt(1);

ASSERT_EQ(1, doc->get_CustomXmlParts()->get_Count());

// Clonar la colección de partes XML y luego usar el método "Clear" para eliminar todos sus elementos de una vez.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPartCollection> customXmlParts = doc->get_CustomXmlParts()->Clone();
customXmlParts->Clear();

// Crear una etiqueta de documento estructurado que muestre el contenido de nuestra parte e insertarla en el cuerpo del documento.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[1]", System::String::Empty);

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CustomXml.docx");
```

## Ver también

* Class [CustomXmlPart](../../customxmlpart/)
* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
