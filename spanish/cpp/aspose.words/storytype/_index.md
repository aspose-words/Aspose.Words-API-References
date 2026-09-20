---
title: "Aspose::Words::StoryType enum"
linktitle: "StoryType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::StoryType enum. El texto de un documento Word se almacena en historias. StoryType identifica una historia en C++."
type: docs
weight: 117000
url: /es/cpp/aspose.words/storytype/
---
## StoryType enum


El texto de un documento Word se almacena en historias. [StoryType](./) identifica una historia.

```cpp
enum class StoryType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | Valor predeterminado. No existe tal historia en el documento. |
| MainText | 1 | Contiene el texto principal del documento, representado por [Body](../body/). |
| Footnotes | 2 | Contiene el texto de la nota al pie, representado por [Footnote](../../aspose.words.notes/footnote/). |
| Endnotes | 3 | Contiene el texto de la nota final, representado por [Footnote](../../aspose.words.notes/footnote/). |
| Comments | 4 | Contiene los comentarios del documento (anotaciones), representado por [Comment](../comment/). |
| Textbox | 5 | Contiene el texto de formas o cuadros de texto, representado por [Shape](../../aspose.words.drawing/shape/). |
| EvenPagesHeader | 6 | Contiene el texto del encabezado de las páginas pares, representado por [HeaderFooter](../headerfooter/). |
| PrimaryHeader | 7 | Contiene el texto del encabezado principal. Cuando el encabezado es diferente para páginas impares y pares, contiene el texto del encabezado de las páginas impares. Representado por [HeaderFooter](../headerfooter/). |
| EvenPagesFooter | 8 | Contiene el texto del pie de página de las páginas pares, representado por [HeaderFooter](../headerfooter/). |
| PrimaryFooter | 9 | Contiene el texto del pie de página principal. Cuando el pie de página es diferente para páginas impares y pares, contiene el texto del pie de página de las páginas impares. Representado por [HeaderFooter](../headerfooter/). |
| FirstPageHeader | 10 | Contiene el texto del encabezado de la primera página, representado por [HeaderFooter](../headerfooter/). |
| FirstPageFooter | 11 | Contiene el texto del pie de página de la primera página, representado por [HeaderFooter](../headerfooter/). |
| FootnoteSeparator | 12 | Contiene el texto del separador de notas al pie. |
| FootnoteContinuationSeparator | 13 | Contiene el texto del separador de continuación de notas al pie. |
| FootnoteContinuationNotice | 14 | Contiene el texto del separador de aviso de continuación de notas al pie. |
| EndnoteSeparator | 15 | Contiene el texto del separador de nota al final. |
| EndnoteContinuationSeparator | 16 | Contiene el texto del separador de continuación de nota al final. |
| EndnoteContinuationNotice | 17 | Contiene el texto del separador de aviso de continuación de nota al final. |


## Ejemplos



Muestra cómo eliminar todas las formas de un nodo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Use un DocumentBuilder para insertar una forma. Esta es una forma en línea,
// que tiene un Paragraph padre, que es un nodo hijo del Body de la primera sección.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Podemos eliminar todas las formas de los párrafos hijos de este Body.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
