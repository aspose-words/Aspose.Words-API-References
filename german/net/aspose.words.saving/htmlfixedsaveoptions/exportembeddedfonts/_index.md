---
title: HtmlFixedSaveOptions.ExportEmbeddedFonts
linktitle: ExportEmbeddedFonts
articleTitle: ExportEmbeddedFonts
second_title: Aspose.Words für .NET
description: Steuern Sie die Einbettung von Schriftarten in Ihr HTML mit der Eigenschaft „ExportEmbeddedFonts“. Verbessern Sie die Dokumentqualität und verwalten Sie gleichzeitig die Dateigröße effektiv.
type: docs
weight: 50
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/
---
## HtmlFixedSaveOptions.ExportEmbeddedFonts property

Gibt an, ob Schriftarten im Base64-Format in HTML-Dokumente eingebettet werden sollen. Beachten Sie, dass das Setzen dieses Flags die Größe der HTML-Ausgabedatei erheblich erhöhen kann.

```csharp
public bool ExportEmbeddedFonts { get; set; }
```

## Beispiele

Zeigt, wie Sie beim Exportieren eines Dokuments in HTML bestimmen, wo eingebettete Schriftarten gespeichert werden sollen.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

// Wenn wir ein Dokument mit eingebetteten Schriftarten nach .html exportieren,
// Aspose.Words kann die Schriftarten an zwei möglichen Stellen platzieren.
// Wenn Sie das Flag „ExportEmbeddedFonts“ auf „true“ setzen, werden die Rohdaten für eingebettete Schriftarten im CSS-Stylesheet gespeichert.
// in der "url"-Eigenschaft der "@font-face"-Regel. Dies kann eine riesige CSS-Stylesheet-Datei erzeugen
// und reduzieren Sie die Anzahl der externen Dateien, die durch diese HTML-Konvertierung erstellt werden.
// Wenn Sie dieses Flag auf „false“ setzen, wird für jede Schriftart eine Datei erstellt.
// Das CSS-Stylesheet verknüpft jede Schriftartdatei mithilfe der „URL“-Eigenschaft der „@font-face“-Regel.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedFonts = exportEmbeddedFonts
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(0, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(2, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
```

### Siehe auch

* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
