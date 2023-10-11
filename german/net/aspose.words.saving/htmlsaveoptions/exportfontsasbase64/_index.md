---
title: HtmlSaveOptions.ExportFontsAsBase64
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt an ob Schriftartressourcen in Base64Kodierung in HTML eingebettet werden sollen. Die Standardeinstellung istFALSCH .
type: docs
weight: 150
url: /de/net/aspose.words.saving/htmlsaveoptions/exportfontsasbase64/
---
## HtmlSaveOptions.ExportFontsAsBase64 property

Gibt an, ob Schriftartressourcen in Base64-Kodierung in HTML eingebettet werden sollen. Die Standardeinstellung ist`FALSCH` .

```csharp
public bool ExportFontsAsBase64 { get; set; }
```

### Bemerkungen

Standardmäßig werden Schriftarten in separate Dateien geschrieben. Wenn diese Option auf eingestellt ist`WAHR`, Schriftarten werden in Base64-Kodierung in das CSS des Dokuments eingebettet .

### Beispiele

Zeigt, wie Schriftarten in ein gespeichertes HTML-Dokument eingebettet werden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontsAsBase64 = true,
    CssStyleSheetType = CssStyleSheetType.Embedded,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

Zeigt, wie ein HTML-Dokument mit darin eingebetteten Bildern gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportImagesAsBase64 = exportImagesAsBase64,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportImagesAsBase64.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportImagesAsBase64.html");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("<img src=\"data:image/png;base64")
    : outDocContents.Contains("<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


