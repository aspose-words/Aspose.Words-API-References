---
title: FootnoteSeparatorCollection Class
linktitle: FootnoteSeparatorCollection
articleTitle: FootnoteSeparatorCollection
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.Notes.FootnoteSeparatorCollection para acceder fácilmente a los separadores de notas al pie en sus documentos. ¡Mejore el formato de sus documentos hoy mismo!
type: docs
weight: 5000
url: /es/net/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class

Proporciona acceso tipificado a[`FootnoteSeparator`](../footnoteseparator/) nodos de un documento.

```csharp
public class FootnoteSeparatorCollection : IEnumerable<FootnoteSeparator>
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FootnoteSeparatorCollection](footnoteseparatorcollection/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Item](../../aspose.words.notes/footnoteseparatorcollection/item/) { get; } | Recupera una[`FootnoteSeparator`](../footnoteseparator/) del tipo especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetEnumerator](../../aspose.words.notes/footnoteseparatorcollection/getenumerator/)() |  |

## Ejemplos

Muestra cómo administrar el formato del separador de notas al pie.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Alinear el separador de notas al pie.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Ver también

* class [FootnoteSeparator](../footnoteseparator/)
* espacio de nombres [Aspose.Words.Notes](../../aspose.words.notes/)
* asamblea [Aspose.Words](../../)
