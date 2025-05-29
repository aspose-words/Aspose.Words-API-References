---
title: StoryType Enum
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.StoryType y gestione fácilmente historias de texto en documentos de Word. ¡Mejore su experiencia de procesamiento de documentos hoy mismo!
type: docs
weight: 6970
url: /es/net/aspose.words/storytype/
---
## StoryType enumeration

El texto de un documento de Word se almacena en historias.`StoryType` identifica una historia.

```csharp
public enum StoryType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Valor predeterminado. No existe tal historia en el documento. |
| MainText | `1` | Contiene el texto principal del documento, representado por[`Body`](../body/) . |
| Footnotes | `2` | Contiene texto de nota al pie, representado por[`Footnote`](../../aspose.words.notes/footnote/) . |
| Endnotes | `3` | Contiene texto de notas finales, representado por[`Footnote`](../../aspose.words.notes/footnote/) . |
| Comments | `4` | Contiene comentarios del documento (anotaciones), representados por[`Comment`](../comment/) . |
| Textbox | `5` | Contiene texto de forma o cuadro de texto, representado por[`Shape`](../../aspose.words.drawing/shape/) . |
| EvenPagesHeader | `6` | Contiene el texto del encabezado de las páginas pares, representado por[`HeaderFooter`](../headerfooter/) . |
| PrimaryHeader | `7` | Contiene el texto del encabezado principal. Si el encabezado es diferente para las páginas pares e impares, contiene el texto del encabezado de las páginas impares. Representado por[`HeaderFooter`](../headerfooter/) . |
| EvenPagesFooter | `8` | Contiene el texto del pie de página de las páginas pares, representado por[`HeaderFooter`](../headerfooter/) . |
| PrimaryFooter | `9` | Contiene el texto del pie de página principal. Si el pie de página es diferente para las páginas pares e impares, contiene el texto del pie de página de las páginas impares. Representado por[`HeaderFooter`](../headerfooter/) . |
| FirstPageHeader | `10` | Contiene el texto del encabezado de la primera página, representado por[`HeaderFooter`](../headerfooter/) . |
| FirstPageFooter | `11` | Contiene el texto del pie de página de la primera página, representado por[`HeaderFooter`](../headerfooter/) . |
| FootnoteSeparator | `12` | Contiene el texto del separador de notas al pie. |
| FootnoteContinuationSeparator | `13` | Contiene el texto del separador de continuación de la nota al pie. |
| FootnoteContinuationNotice | `14` | Contiene el texto del separador del aviso de continuación de la nota al pie. |
| EndnoteSeparator | `15` | Contiene el texto del separador de notas finales. |
| EndnoteContinuationSeparator | `16` | Contiene el texto del separador de continuación de la nota final. |
| EndnoteContinuationNotice | `17` | Contiene el texto del separador del aviso de continuación de la nota final. |

## Ejemplos

Muestra cómo eliminar todas las formas de un nodo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Use un DocumentBuilder para insertar una forma. Esta es una forma en línea.
// que tiene un párrafo padre, que es un nodo hijo del cuerpo de la primera sección.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

//Podemos eliminar todas las formas de los párrafos secundarios de este Cuerpo.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
