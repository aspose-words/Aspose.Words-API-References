---
title: "Aspose::Words::DocumentBuilder::MoveToParagraph método"
linktitle: "MoveToParagraph"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::MoveToParagraph método. Mueve el cursor a un párrafo en la sección actual en C++."
type: docs
weight: 59000
url: /es/cpp/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder::MoveToParagraph method


Mueve el cursor a un párrafo en la sección actual.

```cpp
void Aspose::Words::DocumentBuilder::MoveToParagraph(int32_t paragraphIndex, int32_t characterIndex)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| paragraphIndex | int32_t | El índice del párrafo al que mover. |
| characterIndex | int32_t | El índice del carácter dentro del párrafo. Un valor negativo permite especificar una posición desde el final del párrafo. Usa -1 para mover al final del párrafo. |
## Observaciones


La navegación se realiza dentro de la historia actual de la sección actual. Es decir, si moviste el cursor al encabezado principal de la primera sección, entonces *paragraphIndex* especifica el índice del párrafo dentro de ese encabezado de esa sección.

Cuando *paragraphIndex* es mayor o igual a 0, especifica un índice desde el comienzo de la sección, siendo 0 el primer párrafo. Cuando *paragraphIndex* es menor que 0, especifica un índice desde el final de la sección, siendo -1 el último párrafo.

## Ejemplos



Muestra cómo mover la posición del cursor de un constructor a un párrafo especificado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(22, paragraphs->get_Count());

// Crea un constructor de documentos para editar el documento. El cursor del constructor,
// que es el punto donde insertará nuevos nodos cuando llamemos a sus métodos de construcción de documentos,
// está actualmente al comienzo del documento.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_EQ(0, paragraphs->IndexOf(builder->get_CurrentParagraph()));

// Mover ese cursor a un párrafo diferente colocará el cursor delante de ese párrafo.
builder->MoveToParagraph(2, 0);

// Cualquier contenido nuevo que agreguemos se insertará en ese punto.
builder->Writeln(u"This is a new third paragraph. ");
```

## Ver también

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
