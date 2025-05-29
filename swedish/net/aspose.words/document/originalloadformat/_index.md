---
title: Document.OriginalLoadFormat
linktitle: OriginalLoadFormat
articleTitle: OriginalLoadFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen OriginalLoadFormat för att enkelt komma åt formatet på originaldokumentet som laddats in i ditt objekt, vilket förbättrar dokumenthanteringen.
type: docs
weight: 310
url: /sv/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

Hämtar formatet för originaldokumentet som laddades in i det här objektet.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

## Anmärkningar

Om du skapade ett nytt tomt dokument returnerasDoc värde.

## Exempel

Visar hur man hämtar information om ett dokuments inläsningsoperation.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

### Se även

* enum [LoadFormat](../../loadformat/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
