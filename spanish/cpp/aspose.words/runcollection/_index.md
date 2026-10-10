---
title: "Aspose::Words::RunCollection clase"
linktitle: "RunCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::RunCollection clase. Proporciona acceso tipado a una colección de nodos Run. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 57000
url: /es/cpp/aspose.words/runcollection/
---
## RunCollection class


Proporciona acceso tipado a una colección de nodos [Run](../run/). Para obtener más información, visite el artículo de documentación [Programación con documentos](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class RunCollection : public Aspose::Words::NodeCollection
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
| [idx_get](./idx_get/)(int32_t) | Recupera un [Run](../run/) en el índice dado. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice basado en cero del nodo especificado. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserta un nodo en la colección en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](./toarray/)() | Copia todos los runs de la colección a una nueva matriz de runs. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo determinar el tipo de revisión de un nodo en línea.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// Cuando editamos el documento mientras la opción "Track Changes" encontrada en Revisar -> Seguimiento,
// está activada en Microsoft Word, los cambios que aplicamos cuentan como revisiones.
// Al editar un documento usando Aspose.Words, podemos comenzar a rastrear revisiones mediante
// invocando el método "StartTrackRevisions" del documento y detener el seguimiento usando el método "StopTrackRevisions".
// Podemos aceptar las revisiones para asimilarlas al documento
// o rechazarlas para modificar efectivamente el cambio propuesto.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// El nodo padre de una revisión es el Run al que la revisión se refiere. Un Run es un nodo Inline.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// A continuación se presentan cinco tipos de revisiones que pueden marcar un nodo Inline.
// 1 -  Una revisión "insert".
// Esta revisión ocurre cuando insertamos texto mientras se rastrean los cambios.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  Una revisión "format".
// Esta revisión ocurre cuando cambiamos el formato del texto mientras se rastrean los cambios.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  Una revisión "move from".
// Cuando resaltamos texto en Microsoft Word y luego lo arrastramos a otro lugar del documento
// mientras se rastrean los cambios, aparecen dos revisiones.
// La revisión "move from" es una copia del texto original antes de moverlo.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  Una revisión "move to".
// La revisión "move to" es el texto que movimos a su nueva posición en el documento.
// "Move from" y "move to" aparecen en pares para cada revisión de movimiento que realizamos.
// Aceptar una revisión de movimiento elimina la revisión "move from" y su texto,
// y conserva el texto de la revisión "move to".
// Rechazar una revisión de movimiento, por el contrario, conserva la revisión "move from" y elimina la revisión "move to".
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  Una revisión "delete".
// Esta revisión ocurre cuando eliminamos texto mientras se rastrean los cambios. Cuando eliminamos texto de esta manera,
// permanecerá en el documento como una revisión hasta que aceptemos la revisión,
// lo que eliminará el texto de forma permanente, o rechacemos la revisión, lo que mantendrá el texto que eliminamos en su lugar.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## Ver también

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
