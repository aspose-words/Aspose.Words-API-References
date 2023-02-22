---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlFixedSaveOptions eigendom. Gibt an ob Bilder in ein HTMLDokument im Base64Format eingebettet werden sollen. Beachten Sie dass das Setzen dieses Flags die Größe der AusgabeHtmlDatei erheblich erhöhen kann.
type: docs
weight: 60
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

Gibt an, ob Bilder in ein HTML-Dokument im Base64-Format eingebettet werden sollen. Beachten Sie, dass das Setzen dieses Flags die Größe der Ausgabe-Html-Datei erheblich erhöhen kann.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

### Beispiele

Zeigt, wie Sie beim Exportieren eines Dokuments in HTML bestimmen, wo Bilder gespeichert werden sollen.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Wenn wir ein Dokument mit eingebetteten Bildern in .html exportieren,
// Aspose.Words kann die Bilder an zwei möglichen Orten platzieren.
// Das Setzen des Flags "ExportEmbeddedImages" auf "true" speichert die Rohdaten
// für alle Bilder im Ausgabe-HTML-Dokument im "src"-Attribut von <image> Stichworte.
// Wenn Sie dieses Flag auf "false" setzen, wird für jedes Bild eine Bilddatei im lokalen Dateisystem erstellt,
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
* namensraum [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* Montage [Aspose.Words](../../../)


