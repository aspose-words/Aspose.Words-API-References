---
title: ImportFormatOptions.AdjustSentenceAndWordSpacing
linktitle: AdjustSentenceAndWordSpacing
articleTitle: AdjustSentenceAndWordSpacing
second_title: Aspose.Words para .NET
description: ImportFormatOptions AdjustSentenceAndWordSpacing propiedad. Obtiene o establece un valor booleano que especifica si se debe ajustar el espaciado entre oraciones y palabras automáticamente. El valor predeterminado esFALSO  en C#.
type: docs
weight: 20
url: /es/net/aspose.words/importformatoptions/adjustsentenceandwordspacing/
---
## ImportFormatOptions.AdjustSentenceAndWordSpacing property

Obtiene o establece un valor booleano que especifica si se debe ajustar el espaciado entre oraciones y palabras automáticamente. El valor predeterminado es`FALSO` .

```csharp
public bool AdjustSentenceAndWordSpacing { get; set; }
```

## Ejemplos

Muestra cómo ajustar automáticamente el espaciado entre oraciones y palabras.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(srcDoc);
builder.Write("Dolor sit amet.");

builder = new DocumentBuilder(dstDoc);
builder.Write("Lorem ipsum.");

ImportFormatOptions options = new ImportFormatOptions() { AdjustSentenceAndWordSpacing = true };
builder.InsertDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

Assert.AreEqual("Lorem ipsum. Dolor sit amet.", dstDoc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Ver también

* class [ImportFormatOptions](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
