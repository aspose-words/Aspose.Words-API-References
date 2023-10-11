---
title: Document.PageCount
second_title: Aspose.Words för .NET API Referens
description: Document fast egendom. Hämtar antalet sidor i dokumentet som beräknats av den senaste sidlayoutoperationen.
type: docs
weight: 320
url: /sv/net/aspose.words/document/pagecount/
---
## Document.PageCount property

Hämtar antalet sidor i dokumentet som beräknats av den senaste sidlayoutoperationen.

```csharp
public int PageCount { get; }
```

### Exempel

Visar hur man räknar antalet sidor i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 3");

// Verifiera det förväntade sidantal i dokumentet.
Assert.AreEqual(3, doc.PageCount);

// Att hämta egenskapen PageCount anropade dokumentets sidlayout för att beräkna värdet.
// Denna operation behöver inte göras om när dokumentet återges till ett fast sidsparformat,
// som .pdf. Så du kan spara lite tid, särskilt med mer komplexa dokument.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### Se även

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


