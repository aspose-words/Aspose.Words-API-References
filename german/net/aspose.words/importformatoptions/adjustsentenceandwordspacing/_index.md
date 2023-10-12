---
title: ImportFormatOptions.AdjustSentenceAndWordSpacing
second_title: Aspose.Words für .NET-API-Referenz
description: ImportFormatOptions eigendom. Ruft einen booleschen Wert ab oder legt diesen fest der angibt ob der Satz und Wortabstand automatisch angepasst werden soll. Der Standardwert istFALSCH .
type: docs
weight: 20
url: /de/net/aspose.words/importformatoptions/adjustsentenceandwordspacing/
---
## ImportFormatOptions.AdjustSentenceAndWordSpacing property

Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, ob der Satz- und Wortabstand automatisch angepasst werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool AdjustSentenceAndWordSpacing { get; set; }
```

### Beispiele

Zeigt, wie Satz- und Wortabstände automatisch angepasst werden.

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

### Siehe auch

* class [ImportFormatOptions](../)
* namensraum [Aspose.Words](../../importformatoptions/)
* Montage [Aspose.Words](../../../)


