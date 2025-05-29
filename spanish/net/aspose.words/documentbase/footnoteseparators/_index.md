---
title: DocumentBase.FootnoteSeparators
linktitle: FootnoteSeparators
articleTitle: FootnoteSeparators
second_title: Aspose.Words para .NET
description: Acceda y personalice los separadores de notas al pie y notas finales en su documento con la propiedad FootnoteSeparators de DocumentBase para un mejor control de formato.
type: docs
weight: 40
url: /es/net/aspose.words/documentbase/footnoteseparators/
---
## DocumentBase.FootnoteSeparators property

Proporciona acceso a los separadores de notas al pie/notas finales definidos en el documento.

```csharp
public FootnoteSeparatorCollection FootnoteSeparators { get; }
```

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

* class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* class [DocumentBase](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
