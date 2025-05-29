---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ExportEmbeddedImages i HtmlFixedSaveOptions förbättrar dina HTML-dokument genom att bädda in bilder i Base64-format, vilket optimerar den visuella kvaliteten och hanterar filstorleken.
type: docs
weight: 60
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

Anger om bilder ska bäddas in i ett HTML-dokument i Base64-format. Observera att om du ställer in den här flaggan kan storleken på den utgående HTML-filen ökas avsevärt.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## Exempel

Visar hur man avgör var bilder ska lagras när man exporterar ett dokument till HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// När vi exporterar ett dokument med inbäddade bilder till .html,
// Aspose.Words kan placera bilderna på två möjliga platser.
// Om flaggan "ExportEmbeddedImages" sätts till "true" lagras rådata
// för alla bilder i HTML-dokumentet som utdata, i attributet "src" i taggarna <image>.
// Om denna flagga sätts till "false" skapas en bildfil i det lokala filsystemet för varje bild,
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
