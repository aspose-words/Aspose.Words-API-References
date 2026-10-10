---
title: "Aspose::Words::SectionCollection class"
linktitle: "SectionCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::SectionCollection. Una colección de objetos Section en el documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 59000
url: /es/cpp/aspose.words/sectioncollection/
---
## SectionCollection class


Una colección de objetos [Section](../section/) en el documento. Para obtener más información, visite el artículo de documentación [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class SectionCollection : public Aspose::Words::NodeCollection
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Agrega un nodo al final de la colección. |
| [Clear](../nodecollection/clear/)() | Elimina todos los nodos de esta colección y del documento. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determina si un nodo está en la colección. |
| [get_Count](../nodecollection/get_count/)() | Obtiene el número de nodos en la colección. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Proporciona una iteración simple al estilo "foreach" sobre la colección de nodos. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Recupera una sección en el índice dado. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice basado en cero del nodo especificado. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserta un nodo en la colección en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](./toarray/)() | Copia todas las secciones de la colección a una nueva matriz de secciones. |
| static [Type](./type/)() |  |
## Observaciones


Un documento de Microsoft Word puede contener múltiples secciones. Para crear una sección en Microsoft Word, seleccione el comando Insertar/Salto y elija un tipo de salto. El salto especifica si la sección comienza en una nueva página o en la misma página.

Insertar y eliminar secciones programáticamente puede usarse para personalizar documentos generados durante la combinación de correspondencia. Si un documento necesita tener contenido diferente o partes del contenido según ciertos criterios, puede crear un documento \"maestro\" que contenga múltiples secciones y eliminar algunas de las secciones antes o después de la combinación de correspondencia.

## Ejemplos



Muestra cómo agregar y eliminar secciones en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Elimine la primera sección del documento.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Añada una copia de lo que ahora es la primera sección al final del documento.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Ver también

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
