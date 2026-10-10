---
title: "Aspose::Words::ParagraphCollection clase"
linktitle: "ParagraphCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphCollection clase. Proporciona acceso tipado a una colección de nodos Paragraph. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 48000
url: /es/cpp/aspose.words/paragraphcollection/
---
## ParagraphCollection class


Proporciona acceso tipado a una colección de nodos [Paragraph](../paragraph/). Para obtener más información, visite el artículo de documentación [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class ParagraphCollection : public Aspose::Words::NodeCollection
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
| [idx_get](./idx_get/)(int32_t) | Recupera un [Paragraph](../paragraph/) en el índice especificado. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice basado en cero del nodo especificado. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserta un nodo en la colección en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](./toarray/)() | Copia todos los párrafos de la colección a una nueva matriz de párrafos. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo comprobar si un párrafo es una revisión de movimiento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Este documento contiene revisiones de \"Move\", que aparecen cuando resaltamos texto con el cursor,
// y luego lo arrastramos para moverlo a otra ubicación
// mientras se rastrean revisiones en Microsoft Word mediante \"Review\" -> \"Track changes\".
ASSERT_EQ(6, doc->get_Revisions()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Revision>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Revision> r)>>([](System::SharedPtr<Aspose::Words::Revision> r) -> bool
{
    return r->get_RevisionType() == Aspose::Words::RevisionType::Moving;
}))));

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// Las revisiones de movimiento consisten en pares de revisiones \"Move from\" y \"Move to\".
// Estas revisiones son cambios potenciales en el documento que podemos aceptar o rechazar.
// Antes de aceptar/rechazar una revisión de movimiento, el documento
// debe llevar un registro de los destinos de salida y llegada del texto.
// El segundo y el cuarto párrafo definen una de esas revisiones, y por lo tanto ambos tienen el mismo contenido.
ASSERT_EQ(paragraphs->idx_get(1)->GetText(), paragraphs->idx_get(3)->GetText());

// La revisión \"Move from\" es el párrafo del cual arrastramos el texto.
// Si aceptamos la revisión, este párrafo desaparecerá,
// y el otro permanecerá y ya no será una revisión.
ASSERT_TRUE(paragraphs->idx_get(1)->get_IsMoveFromRevision());

// La revisión \"Move to\" es el párrafo al que arrastramos el texto.
// Si rechazamos la revisión, este párrafo, en su lugar, desaparecerá, y el otro permanecerá.
ASSERT_TRUE(paragraphs->idx_get(3)->get_IsMoveToRevision());
```

## Ver también

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
