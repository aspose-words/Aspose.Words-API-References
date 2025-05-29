---
title: FootnoteSeparatorCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words para .NET
description: Acceda a la propiedad de elemento FootnoteSeparatorCollection para recuperar fácilmente FootnoteSeparators personalizados por tipo, mejorando así el formato de su documento.
type: docs
weight: 20
url: /es/net/aspose.words.notes/footnoteseparatorcollection/item/
---
## FootnoteSeparatorCollection indexer

Recupera una[`FootnoteSeparator`](../../footnoteseparator/) del tipo especificado.

```csharp
public FootnoteSeparator this[FootnoteSeparatorType separatorType] { get; }
```

## Observaciones

Devuelve`nulo` Si no se encuentra el separador de notas al pie/nota final del tipo especificado.

## Ejemplos

Muestra cómo administrar el formato del separador de notas al pie.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Alinear el separador de notas al pie.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Ver también

* class [FootnoteSeparator](../../footnoteseparator/)
* enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* class [FootnoteSeparatorCollection](../)
* espacio de nombres [Aspose.Words.Notes](../../../aspose.words.notes/)
* asamblea [Aspose.Words](../../../)
