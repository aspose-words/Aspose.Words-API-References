---
title: HtmlSaveOptions.FontsFolderAlias
linktitle: FontsFolderAlias
articleTitle: FontsFolderAlias
second_title: Aspose.Words für .NET
description: Entdecken Sie die HtmlSaveOptions FontsFolderAlias-Eigenschaft, um Schrift-URIs in Ihren HTML-Dokumenten anzupassen. Verbessern Sie Ihr Webdesign im Handumdrehen!
type: docs
weight: 320
url: /de/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

Gibt den Namen des Ordners an, der zum Erstellen von Schriftart-URIs verwendet wird, die in ein HTML-Dokument geschrieben werden. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string FontsFolderAlias { get; set; }
```

## Bemerkungen

Wenn Sie eine[`Document`](../../../aspose.words/document/) im HTML-Format und[`ExportFontResources`](../exportfontresources/) ist eingestellt auf`WAHR` , Aspose.Words muss die im Dokument verwendeten Schriftarten als eigenständige Dateien speichern. [`FontsFolder`](../fontsfolder/) ermöglicht Ihnen, anzugeben, wo die Schriftarten gespeichert werden und `FontsFolderAlias` ermöglicht die Angabe, wie die Schriftart-URIs erstellt werden.

Wenn`FontsFolderAlias` ist keine leere Zeichenfolge, dann wird die Schriftart-URI geschrieben in HTMLFontsFolderAlias + &lt;Schriftdateiname&gt;.

Wenn`FontsFolderAlias` ist eine leere Zeichenfolge, dann wird die Schriftart-URI written in HTMLFontsFolder + &lt;Schriftdateiname&gt;.

Wenn`FontsFolderAlias`auf „.“ (Punkt) gesetzt ist, wird der Schriftdateiname ohne Pfad in HTML geschrieben, unabhängig von anderen Optionen.

Alternativ können Sie den Namen des Ordners angeben, um die Schriftart-URIs zu erstellen. Verwenden Sie dazu[`ResourceFolderAlias`](../resourcefolderalias/).

## Beispiele

Zeigt, wie Ordner und Ordneraliase für extern gespeicherte Ressourcen festgelegt werden, die Aspose.Words beim Speichern eines Dokuments im HTML-Format erstellt.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    ImageResolution = 72,
    FontResourcesSubsettingSizeThreshold = 0,
    FontsFolder = ArtifactsDir + "Fonts",
    ImagesFolder = ArtifactsDir + "Images",
    ResourceFolder = ArtifactsDir + "Resources",
    FontsFolderAlias = "http://example.com/fonts",
    ImagesFolderAlias = "http://example.com/images",
    ResourceFolderAlias = "http://example.com/resources",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
