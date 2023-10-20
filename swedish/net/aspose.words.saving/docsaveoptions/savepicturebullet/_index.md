---
title: DocSaveOptions.SavePictureBullet
linktitle: SavePictureBullet
articleTitle: SavePictureBullet
second_title: Aspose.Words för .NET
description: DocSaveOptions SavePictureBullet fast egendom. Närfalsk  PictureBulletdata sparas inte i utdatadokumentet. Standardvärdet ärSann  i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

När`falsk` , PictureBullet-data sparas inte i utdatadokumentet. Standardvärdet är`Sann` .

```csharp
public bool SavePictureBullet { get; set; }
```

## Anmärkningar

Det här alternativet finns för Word 97, som inte fungerar korrekt med PictureBullet-data. För att ta bort PictureBullet-data, ställ in alternativet på "false".

## Exempel

Visar hur du utelämnar PictureBullet-data från dokumentet när du sparar.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");
// Vissa ordbehandlare, som Microsoft Word 97, är inkompatibla med PictureBullet-data.
// Genom att sätta en flagga i SaveOptions-objektet,
// vi kan konvertera alla bildpunkter till vanliga punktpunkter samtidigt som vi sparar.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### Se även

* class [DocSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
