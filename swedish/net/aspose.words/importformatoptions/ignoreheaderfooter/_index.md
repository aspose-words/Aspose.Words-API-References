---
title: ImportFormatOptions.IgnoreHeaderFooter
second_title: Aspose.Words för .NET API Referens
description: ImportFormatOptions fast egendom. Hämtar eller ställer in ett booleskt värde som anger att källformateringen av sidhuvuden/sidfotsinnehåll ignoreras omKeepSourceFormatting läge används. Standardvärdet ärSann .
type: docs
weight: 40
url: /sv/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Hämtar eller ställer in ett booleskt värde som anger att källformateringen av sidhuvuden/sidfotsinnehåll ignoreras omKeepSourceFormatting läge används. Standardvärdet är`Sann` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

### Exempel

Visar hur man anger att ignorera eller inte källformatering av sidhuvuden/sidfotsinnehåll.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### Se även

* class [ImportFormatOptions](../)
* namnutrymme [Aspose.Words](../../importformatoptions/)
* hopsättning [Aspose.Words](../../../)


