---
title: ExportFontsAsBase64
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt an ob Schriftartressourcen in HTML in Base64-Codierung eingebettet werden sollen. Standard istFALSCH .
type: docs
weight: 160
url: /de/net/aspose.words.saving/htmlsaveoptions/exportfontsasbase64/
---
## HtmlSaveOptions.ExportFontsAsBase64 property

Gibt an, ob Schriftartressourcen in HTML in Base64-Codierung eingebettet werden sollen. Standard ist`FALSCH` .

```csharp
public bool ExportFontsAsBase64 { get; set; }
```

### Bemerkungen

Standardmäßig werden Schriftarten in separate Dateien geschrieben. Wenn diese Option auf eingestellt ist`Stimmt`, Schriftarten werden in das CSS des Dokuments in Base64-Codierung eingebettet .

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

* class [HtmlSaveOptions](../../htmlsaveoptions)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->