---
title: RtfSaveOptions.SaveImagesAsWmf
linktitle: SaveImagesAsWmf
articleTitle: SaveImagesAsWmf
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen RtfSaveOptions SaveImagesAsWmf förbättrar ditt dokument genom att spara alla bilder som WMF för överlägsen kvalitet och kompatibilitet.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/rtfsaveoptions/saveimagesaswmf/
---
## RtfSaveOptions.SaveImagesAsWmf property

När`sann` Alla bilder kommer att sparas som WMF.

```csharp
public bool SaveImagesAsWmf { get; set; }
```

## Anmärkningar

Det här alternativet kan hjälpa till att undvika varningsmeddelanden i WordPad.

## Exempel

Visar hur man konverterar alla bilder i ett dokument till Windows Metafile-format när vi sparar dokumentet som en RTF-fil.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg");

Assert.AreEqual(ImageType.Jpeg, imageShape.ImageData.ImageType);

builder.InsertParagraph();
builder.Writeln("Png image:");
imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ImageType.Png, imageShape.ImageData.ImageType);

// Skapa ett "RtfSaveOptions"-objekt som ska skickas till dokumentets "Save"-metod för att ändra hur vi sparar det till en RTF-fil.
RtfSaveOptions rtfSaveOptions = new RtfSaveOptions();

// Sätt egenskapen "SaveImagesAsWmf" till "true" för att konvertera alla bilder i dokumentet till WMF när vi sparar det i RTF.
// Att göra det kommer att hjälpa läsare som WordPad att läsa vårt dokument.
// Sätt egenskapen "SaveImagesAsWmf" till "false" för att bevara originalformatet för alla bilder i dokumentet.
// eftersom vi sparar det i RTF-format. Detta kommer att bevara bildernas kvalitet på bekostnad av kompatibilitet med äldre RTF-läsare.
rtfSaveOptions.SaveImagesAsWmf = saveImagesAsWmf;

doc.Save(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf", rtfSaveOptions);

doc = new Document(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf");

NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

if (saveImagesAsWmf)
{
    Assert.AreEqual(ImageType.Wmf, ((Shape)shapes[0]).ImageData.ImageType);
    Assert.AreEqual(ImageType.Wmf, ((Shape)shapes[1]).ImageData.ImageType);
}
else
{
    Assert.AreEqual(ImageType.Jpeg, ((Shape)shapes[0]).ImageData.ImageType);
    Assert.AreEqual(ImageType.Png, ((Shape)shapes[1]).ImageData.ImageType);
}
```

### Se även

* class [RtfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
