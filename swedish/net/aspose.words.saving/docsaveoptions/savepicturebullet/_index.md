---
title: DocSaveOptions.SavePictureBullet
linktitle: SavePictureBullet
articleTitle: SavePictureBullet
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen SavePictureBullet i DocSaveOptions förbättrar dina dokumentresultat. Kontrollera enkelt datasparandet i PictureBullet för optimala resultat.
type: docs
weight: 60
url: /sv/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

När`falsk` , PictureBullet-data sparas inte i utdatadokumentet. Standardvärdet är`sann` .

```csharp
public bool SavePictureBullet { get; set; }
```

## Anmärkningar

Det här alternativet finns för Word 97, som inte fungerar korrekt med PictureBullet-data. För att ta bort PictureBullet-data, sätt alternativet till "false".

## Exempel

Visar hur man utelämnar PictureBullet-data från dokumentet när man sparar.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");
// Vissa ordbehandlare, som Microsoft Word 97, är inkompatibla med PictureBullet-data.
// Genom att sätta en flagga i SaveOptions-objektet,
// vi kan konvertera alla bildpunkter till vanliga punkter medan vi sparar.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### Se även

* class [DocSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
