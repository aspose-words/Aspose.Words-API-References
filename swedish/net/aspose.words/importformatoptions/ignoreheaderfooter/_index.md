---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ImportFormatOptions IgnoreHeaderFooter, styr formateringen av sidhuvud/sidfot i KeepSourceFormatting-läget. Förenkla dina dokumentimporter idag!
type: docs
weight: 40
url: /sv/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Hämtar eller ställer in ett booleskt värde som anger att källformateringen av innehållet i sidhuvuden/sidfoten ignoreras. omKeepSourceFormatting läget används. Standardvärdet är`sann` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## Exempel

Visar hur man anger om källformatering för innehåll i sidhuvuden/sidfot ska ignoreras eller inte.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

// Om 'IgnoreHeaderFooter' är falskt så är den ursprungliga formateringen för sidhuvud/sidfot
// från "Subtitlar och sidfotstyper.docx" kommer att användas.
// Om 'IgnoreHeaderFooter' är sant så gäller formateringen för sidhuvud/sidfot
// från "Document.docx" kommer att användas.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### Se även

* class [ImportFormatOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
