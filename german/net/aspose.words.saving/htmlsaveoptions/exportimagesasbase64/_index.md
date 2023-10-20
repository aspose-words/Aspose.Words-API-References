---
title: HtmlSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words für .NET
description: HtmlSaveOptions ExportImagesAsBase64 eigendom. Gibt an ob Bilder im Base64Format in der AusgabeHTML MHTML oder EPUB gespeichert werden. Standard istFALSCH  in C#.
type: docs
weight: 170
url: /de/net/aspose.words.saving/htmlsaveoptions/exportimagesasbase64/
---
## HtmlSaveOptions.ExportImagesAsBase64 property

Gibt an, ob Bilder im Base64-Format in der Ausgabe-HTML, MHTML oder EPUB gespeichert werden. Standard ist`FALSCH` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Bemerkungen

Wenn diese Eigenschaft auf festgelegt ist`WAHR` Bilddaten werden direkt in das exportiert **Bild** Elemente und separate Dateien werden nicht erstellt.

## Beispiele

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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
