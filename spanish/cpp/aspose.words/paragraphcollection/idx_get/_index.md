---
title: "Aspose::Words::ParagraphCollection::idx_get método"
linktitle: "idx_get"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphCollection::idx_get método. Recupera un Paragraph en el índice dado en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/paragraphcollection/idx_get/
---
## ParagraphCollection::idx_get method


Recupera un [Paragraph](../../paragraph/) en el índice dado.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::ParagraphCollection::idx_get(int32_t index)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | Un índice en la colección. |
## Observaciones


El índice comienza en cero.

Se permiten índices negativos e indican acceso desde el final de la colección. Por ejemplo, -1 significa el último elemento, -2 el penúltimo y así sucesivamente.

Si el índice es mayor o igual que el número de elementos en la lista, esto devuelve una referencia nula.

Si el índice es negativo y su valor absoluto es mayor que el número de elementos en la lista, esto devuelve una referencia nula.

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

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
