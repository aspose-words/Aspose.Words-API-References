---
title: FootnoteSeparatorType Enum
linktitle: FootnoteSeparatorType
articleTitle: FootnoteSeparatorType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.FootnoteSeparatorType para personalizar los separadores de notas al pie y notas finales, mejorando el formato y la legibilidad del documento.
type: docs
weight: 5010
url: /es/net/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enumeration

Especifica el tipo de separador de notas al pie/notas finales.

```csharp
public enum FootnoteSeparatorType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| FootnoteSeparator | `0` | Separador entre el texto principal y el texto de la nota al pie. |
| FootnoteContinuationSeparator | `1` | Se imprime encima del texto de la nota al pie de una página cuando el texto debe continuar desde una página anterior. |
| FootnoteContinuationNotice | `2` | Se imprime debajo del texto de la nota al pie en una página cuando el texto de la nota al pie debe continuar en una página siguiente. |
| EndnoteSeparator | `3` | Separador entre el texto principal y el texto de la nota final. |
| EndnoteContinuationSeparator | `4` | Impreso encima del texto de la nota final en una página cuando el texto debe continuar desde una página anterior. |
| EndnoteContinuationNotice | `5` | Se imprime debajo del texto de la nota final en una página cuando el texto de la nota final debe continuar en una página siguiente. |

## Ejemplos

Muestra cómo eliminar el separador de notas finales.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator endnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.EndnoteSeparator];
// Eliminar el separador de notas finales.
endnoteSeparator.FirstParagraph.FirstChild.Remove();
```

Muestra cómo administrar el formato del separador de notas al pie.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Alinear el separador de notas al pie.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Ver también

* espacio de nombres [Aspose.Words.Notes](../../aspose.words.notes/)
* asamblea [Aspose.Words](../../)
