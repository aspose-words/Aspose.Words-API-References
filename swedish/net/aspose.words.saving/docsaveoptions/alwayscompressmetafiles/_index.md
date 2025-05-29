---
title: DocSaveOptions.AlwaysCompressMetafiles
linktitle: AlwaysCompressMetafiles
articleTitle: AlwaysCompressMetafiles
second_title: Aspose.Words för .NET
description: Optimera din dokumenthantering med egenskapen AlwaysCompressMetafiles. Förbättra prestandan genom att kontrollera metafilkomprimering för effektivitet.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

När`falsk` , små metafiler komprimeras inte av prestandaskäl. Standardvärdet är`sann` , alla metafiler komprimeras oavsett storlek.

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

## Exempel

Visar hur man ändrar komprimering av metafiler i ett dokument när man sparar.

```csharp
// Öppna ett dokument som innehåller en Microsoft Equation 3.0-formel.
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// När vi sparar ett dokument komprimeras inte mindre metafiler av prestandaskäl.
// Vi kan sätta en flagga i ett SaveOptions-objekt för att komprimera varje metafil vid sparning.
// Vissa editorer som LibreOffice kan inte läsa okomprimerade metafiler.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

### Se även

* class [DocSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
