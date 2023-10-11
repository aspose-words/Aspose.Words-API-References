---
title: HtmlSaveOptions.ExportCidUrlsForMhtmlResources
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt an ob CIDURLs ContentID zum Verweisen auf Ressourcen Bilder Schriftarten CSS verwendet werden sollen die in MHTML Dokumenten enthalten sind. Der Standardwert istFALSCH .
type: docs
weight: 110
url: /de/net/aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/
---
## HtmlSaveOptions.ExportCidUrlsForMhtmlResources property

Gibt an, ob CID-URLs (Content-ID) zum Verweisen auf Ressourcen (Bilder, Schriftarten, CSS) verwendet werden sollen, die in MHTML -Dokumenten enthalten sind. Der Standardwert ist`FALSCH` .

```csharp
public bool ExportCidUrlsForMhtmlResources { get; set; }
```

### Bemerkungen

Diese Option betrifft nur Dokumente, die im MHTML-Format gespeichert werden.

Standardmäßig werden Ressourcen in MHTML-Dokumenten durch Dateinamen referenziert (z. B. „image.png“), die mit „Content-Location“-Headern von MIME-Teilen abgeglichen werden.

Diese Option aktiviert eine alternative Methode, bei der Verweise auf Ressourcendateien als CID (Content-ID) -URLs geschrieben werden (z. B. „cid:image.png“) und mit „Content-ID“-Headern abgeglichen werden.

Theoretisch sollte es keinen Unterschied zwischen den beiden Referenzierungsmethoden geben und beide sollten in jedem Browser oder Mail-Agenten einwandfrei funktionieren. In der Praxis gelingt es einigen Agenten jedoch nicht, Ressourcen anhand des Dateinamens abzurufen. Wenn Ihr -Browser oder E-Mail-Agent das Laden von in einem MTHML-Dokument enthaltenen Ressourcen ablehnt (keine Bilder anzeigt oder keine CSS-Stile lädt), versuchen Sie, das Dokument mit CID-URLs zu exportieren.

### Beispiele

Zeigt, wie Inhalts-IDs für ausgegebene MHTML-Dokumente aktiviert werden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Durch Setzen dieses Flags werden die „Content-Location“-Tags ersetzt
// mit „Content-ID“-Tags für jede Ressource aus dem Eingabedokument.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mhtml)
{
    ExportCidUrlsForMhtmlResources = exportCidUrlsForMhtmlResources,
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    Assert.True(outDocContents.Contains("Content-ID: <document.html>"));
    Assert.True(outDocContents.Contains("<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    Assert.True(outDocContents.Contains("Content-Location: document.html"));
    Assert.True(outDocContents.Contains("<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


