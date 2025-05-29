---
title: Document.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Dokumentsidaantal, som visar det totala sidantalet baserat på den senaste layouten, vilket säkerställer korrekt dokumenthantering och insikter.
type: docs
weight: 330
url: /sv/net/aspose.words/document/pagecount/
---
## Document.PageCount property

Hämtar antalet sidor i dokumentet beräknat med den senaste sidlayoutoperationen.

```csharp
public int PageCount { get; }
```

## Exempel

Visar hur man räknar antalet sidor i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 3");

// Verifiera dokumentets förväntade sidantal.
Assert.AreEqual(3, doc.PageCount);

// Att hämta PageCount-egenskapen anropade dokumentets sidlayout för att beräkna värdet.
// Denna operation behöver inte göras om när dokumentet renderas till ett fast sidformat för att spara sidor,
// som till exempel .pdf. Så du kan spara tid, särskilt med mer komplexa dokument.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### Se även

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
