---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words für .NET
description: HtmlFixedSaveOptions ExportEmbeddedImages eigendom. Gibt an ob Bilder in ein HTMLDokument im Base64Format eingebettet werden sollen. Hinweis Das Setzen dieses Flags kann die Größe der ausgegebenen HTMLDatei erheblich erhöhen in C#.
type: docs
weight: 60
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

Gibt an, ob Bilder in ein HTML-Dokument im Base64-Format eingebettet werden sollen. Hinweis: Das Setzen dieses Flags kann die Größe der ausgegebenen HTML-Datei erheblich erhöhen.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## Beispiele

Zeigt, wie Sie bestimmen, wo Bilder gespeichert werden sollen, wenn Sie ein Dokument in HTML exportieren.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Wenn wir ein Dokument mit eingebetteten Bildern nach .html exportieren,
// Aspose.Words kann die Bilder an zwei möglichen Orten platzieren.
// Wenn Sie das Flag „ExportEmbeddedImages“ auf „true“ setzen, werden die Rohdaten gespeichert
// für alle Bilder im ausgegebenen HTML-Dokument im „src“-Attribut von <image> Stichworte.
// Wenn Sie dieses Flag auf „false“ setzen, wird für jedes Bild eine Bilddatei im lokalen Dateisystem erstellt.
// und alle diese Dateien in einem separaten Ordner speichern.
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
