---
title: RtfSaveOptions.SaveImagesAsWmf
linktitle: SaveImagesAsWmf
articleTitle: SaveImagesAsWmf
second_title: Aspose.Words för .NET
description: RtfSaveOptions SaveImagesAsWmf fast egendom. NärSann alla bilder kommer att sparas som WMF i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/rtfsaveoptions/saveimagesaswmf/
---
## RtfSaveOptions.SaveImagesAsWmf property

När`Sann` alla bilder kommer att sparas som WMF.

```csharp
public bool SaveImagesAsWmf { get; set; }
```

## Anmärkningar

Det här alternativet kan hjälpa till att undvika WordPad-varningsmeddelanden.

## Exempel

Visar hur man konverterar alla bilder i ett dokument till Windows Metafile-format när vi sparar dokumentet som en RTF.

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

// Skapa ett "RtfSaveOptions"-objekt för att skicka till dokumentets "Save"-metod för att ändra hur vi sparar det till en RTF.
RtfSaveOptions rtfSaveOptions = new RtfSaveOptions();

// Ställ in egenskapen "SaveImagesAsWmf" till "true" för att konvertera alla bilder i dokumentet till WMF när vi sparar det till RTF.
// Om du gör det hjälper läsare som WordPad att läsa vårt dokument.
// Ställ in egenskapen "SaveImagesAsWmf" till "false" för att bevara originalformatet för alla bilder i dokumentet
// när vi sparar det till RTF. Detta kommer att bevara kvaliteten på bilderna på bekostnad av kompatibilitet med äldre RTF-läsare.
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
