---
title: "Método Aspose::Words::InlineStory::get_IsDeleteRevision"
linktitle: "get_IsDeleteRevision"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::InlineStory::get_IsDeleteRevision. Devuelve true si este objeto fue eliminado en Microsoft Word mientras el seguimiento de cambios estaba habilitado en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/inlinestory/get_isdeleterevision/
---
## InlineStory::get_IsDeleteRevision method


Devuelve true si este objeto fue eliminado en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```cpp
bool Aspose::Words::InlineStory::get_IsDeleteRevision()
```


## Ejemplos



Muestra cómo ver las propiedades relacionadas con revisiones de los nodos [InlineStory](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision footnotes.docx");

// Cuando editamos el documento mientras la opción "Track Changes" encontrada en Revisar -> Seguimiento,
// está activada en Microsoft Word, los cambios que aplicamos cuentan como revisiones.
// Al editar un documento usando Aspose.Words, podemos comenzar a rastrear revisiones mediante
// invocando el método "StartTrackRevisions" del documento y detener el seguimiento usando el método "StopTrackRevisions".
// Podemos aceptar las revisiones para asimilarlas al documento
// o rechazarlos para deshacer y descartar el cambio propuesto.
ASSERT_TRUE(doc->get_HasRevisions());

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Notes::Footnote>>> footnotes = doc->GetChildNodes(Aspose::Words::NodeType::Footnote, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Notes::Footnote> >()->LINQ_ToList();

ASSERT_EQ(5, footnotes->get_Count());

// A continuación se presentan cinco tipos de revisiones que pueden marcar un nodo InlineStory.
// 1 -  Una revisión "insert".
// Esta revisión ocurre cuando insertamos texto mientras se rastrean los cambios.
ASSERT_TRUE(footnotes->idx_get(2)->get_IsInsertRevision());

// 2 -  Una revisión de "mover desde":
// Cuando resaltamos texto en Microsoft Word y luego lo arrastramos a otro lugar del documento
// mientras se rastrean los cambios, aparecen dos revisiones.
// La revisión "move from" es una copia del texto original antes de moverlo.
ASSERT_TRUE(footnotes->idx_get(4)->get_IsMoveFromRevision());

// 3 -  Una revisión de "mover a":
// La revisión "move to" es el texto que movimos a su nueva posición en el documento.
// "Move from" y "move to" aparecen en pares para cada revisión de movimiento que realizamos.
// Aceptar una revisión de movimiento elimina la revisión "move from" y su texto,
// y conserva el texto de la revisión "move to".
// Rechazar una revisión de movimiento, por el contrario, conserva la revisión "move from" y elimina la revisión "move to".
ASSERT_TRUE(footnotes->idx_get(1)->get_IsMoveToRevision());

// 4 -  Una revisión de "eliminar":
// Esta revisión ocurre cuando eliminamos texto mientras se rastrean los cambios. Cuando eliminamos texto de esta manera,
// permanecerá en el documento como una revisión hasta que aceptemos la revisión,
// lo que eliminará el texto de forma permanente, o rechacemos la revisión, lo que mantendrá el texto que eliminamos en su lugar.
ASSERT_TRUE(footnotes->idx_get(3)->get_IsDeleteRevision());
```

## Ver también

* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
