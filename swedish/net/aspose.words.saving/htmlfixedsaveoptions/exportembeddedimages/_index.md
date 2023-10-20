---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words för .NET
description: HtmlFixedSaveOptions ExportEmbeddedImages fast egendom. Anger om bilder ska bäddas in i HTMLdokument i Base64format. Observera att denna flagga kan öka storleken på utdatafilen avsevärt i C#.
type: docs
weight: 60
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

Anger om bilder ska bäddas in i HTML-dokument i Base64-format. Observera att denna flagga kan öka storleken på utdatafilen avsevärt.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## Exempel

Visar hur man bestämmer var bilder ska lagras vid export av ett dokument till HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// När vi exporterar ett dokument med inbäddade bilder till .html,
// Aspose.Words kan placera bilderna på två möjliga platser.
// Om du ställer in "ExportEmbeddedImages"-flaggan till "true" lagras rådata
// för alla bilder i det utgående HTML-dokumentet, i "src"-attributet för <image> taggar.
// Om du ställer in denna flagga på "false" skapas en bildfil i det lokala filsystemet för varje bild,
// och lagra alla dessa filer i en separat mapp.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedImages = exportImages
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" " +
        "src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />").Success);
}
```

### Se även

* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
