---
title: HtmlFixedSaveOptions.ExportEmbeddedFonts
linktitle: ExportEmbeddedFonts
articleTitle: ExportEmbeddedFonts
second_title: Aspose.Words für .NET
description: HtmlFixedSaveOptions ExportEmbeddedFonts eigendom. Gibt an ob Schriftarten in ein HTMLDokument im Base64Format eingebettet werden sollen. Hinweis Das Setzen dieses Flags kann die Größe der ausgegebenen HTMLDatei erheblich erhöhen in C#.
type: docs
weight: 50
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/
---
## HtmlFixedSaveOptions.ExportEmbeddedFonts property

Gibt an, ob Schriftarten in ein HTML-Dokument im Base64-Format eingebettet werden sollen. Hinweis: Das Setzen dieses Flags kann die Größe der ausgegebenen HTML-Datei erheblich erhöhen.

```csharp
public bool ExportEmbeddedFonts { get; set; }
```

## Beispiele

Zeigt, wie Sie bestimmen, wo eingebettete Schriftarten gespeichert werden sollen, wenn Sie ein Dokument in HTML exportieren.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

// Wenn wir ein Dokument mit eingebetteten Schriftarten nach .html exportieren,
// Aspose.Words kann die Schriftarten an zwei möglichen Orten platzieren.
// Wenn Sie das Flag „ExportEmbeddedFonts“ auf „true“ setzen, werden die Rohdaten für eingebettete Schriftarten im CSS-Stylesheet gespeichert.
// in der Eigenschaft „url“ der Regel „@font-face“. Dadurch kann eine riesige CSS-Stylesheet-Datei entstehen
// und reduzieren Sie die Anzahl der externen Dateien, die diese HTML-Konvertierung erstellt.
// Wenn Sie dieses Flag auf „false“ setzen, wird für jede Schriftart eine Datei erstellt.
// Das CSS-Stylesheet stellt mithilfe der „url“-Eigenschaft der „@font-face“-Regel eine Verknüpfung zu jeder Schriftartendatei her.
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
