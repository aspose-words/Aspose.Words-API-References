---
title: DocSaveOptions.AlwaysCompressMetafiles
second_title: Aspose.Words för .NET API Referens
description: DocSaveOptions fast egendom. Närfalsk  små metafiler komprimeras inte av prestandaskäl. Standardvärdet ärSann  alla metafiler komprimeras oavsett storlek.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

När`falsk` , små metafiler komprimeras inte av prestandaskäl. Standardvärdet är`Sann` , alla metafiler komprimeras oavsett storlek.

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

### Exempel

Visar hur du ändrar metafilers komprimering i ett dokument medan du sparar.

```csharp
// Öppna ett dokument som innehåller en Microsoft Equation 3.0-formel.
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// När vi sparar ett dokument komprimeras inte mindre metafiler av prestandaskäl.
// Vi kan sätta en flagga i ett SaveOptions-objekt för att komprimera varje metafil när du sparar.
// Vissa redigerare som LibreOffice kan inte läsa okomprimerade metafiler.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);

if (compressAllMetafiles)
    Assert.That(10000, Is.LessThan(new FileInfo(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx").Length));
else
    Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx").Length));
```

### Se även

* class [DocSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../docsaveoptions/)
* hopsättning [Aspose.Words](../../../)


