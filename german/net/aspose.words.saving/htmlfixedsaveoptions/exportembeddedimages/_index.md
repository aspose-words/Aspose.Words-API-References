---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „ExportEmbeddedImages“ in „HtmlFixedSaveOptions“ Ihre HTML-Dokumente verbessert, indem sie Bilder im Base64-Format einbettet und so die visuelle Qualität optimiert und gleichzeitig die Dateigröße verwaltet.
type: docs
weight: 60
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

Gibt an, ob Bilder in HTML-Dokumente im Base64-Format eingebettet werden sollen. Beachten Sie, dass das Setzen dieses Flags die Größe der HTML-Ausgabedatei erheblich erhöhen kann.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## Beispiele

Zeigt, wie Sie beim Exportieren eines Dokuments in HTML bestimmen, wo Bilder gespeichert werden sollen.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Wenn wir ein Dokument mit eingebetteten Bildern in .html exportieren,
// Aspose.Words kann die Bilder an zwei möglichen Orten platzieren.
// Wenn Sie das Flag "ExportEmbeddedImages" auf "true" setzen, werden die Rohdaten gespeichert
// für alle Bilder im HTML-Ausgabedokument, im „src“-Attribut der <image>-Tags.
// Wenn Sie dieses Flag auf „false“ setzen, wird für jedes Bild eine Bilddatei im lokalen Dateisystem erstellt.
// und speichern Sie alle diese Dateien in einem separaten Ordner.
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

### Siehe auch

* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
