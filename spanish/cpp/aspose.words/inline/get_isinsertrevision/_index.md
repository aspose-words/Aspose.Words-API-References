---
title: "Aspose::Words::Inline::get_IsInsertRevision método"
linktitle: "get_IsInsertRevision"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Inline::get_IsInsertRevision. Devuelve true si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/inline/get_isinsertrevision/
---
## Inline::get_IsInsertRevision method


Devuelve true si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```cpp
bool Aspose::Words::Inline::get_IsInsertRevision()
```


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

* Class [Inline](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
