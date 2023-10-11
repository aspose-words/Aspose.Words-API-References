---
title: HtmlSaveOptions.FontsFolderAlias
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt den Namen des Ordners an der zum Erstellen von SchriftartURIs verwendet wird die in ein HTMLDokument geschrieben werden. Der Standardwert ist eine leere Zeichenfolge.
type: docs
weight: 320
url: /de/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

Gibt den Namen des Ordners an, der zum Erstellen von Schriftart-URIs verwendet wird, die in ein HTML-Dokument geschrieben werden. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string FontsFolderAlias { get; set; }
```

### Bemerkungen

Wenn Sie a speichern[`Document`](../../../aspose.words/document/) im HTML-Format und[`ExportFontResources`](../exportfontresources/) ist eingestellt auf`WAHR` , Aspose.Words muss die im Dokument verwendeten Schriftarten als eigenständige Dateien speichern. [`FontsFolder`](../fontsfolder/) Hier können Sie angeben, wo die Schriftarten gespeichert werden und `FontsFolderAlias` ermöglicht die Angabe, wie die Schriftart-URIs erstellt werden.

Wenn`FontsFolderAlias` kein leerer String ist, wird der Schriftart-URI in HTML geschrieben angezeigtFontsFolderAlias + &lt;Name der Schriftartdatei&gt;.

Wenn`FontsFolderAlias` eine leere Zeichenfolge ist, wird der in HTML geschriebene Schriftart-URI seinFontsFolder + &lt;Name der Schriftartdatei&gt;.

Wenn`FontsFolderAlias`ist eingestellt auf '.' (Punkt), dann wird der Schriftdateiname unabhängig von anderen Optionen ohne Pfad in HTML geschrieben.

Eine alternative Möglichkeit, den Namen des Ordners zum Erstellen der Schriftart-URIs anzugeben, ist die Verwendung[`ResourceFolderAlias`](../resourcefolderalias/).

### Beispiele

Zeigt, wie Ordner und Ordneraliase für extern gespeicherte Ressourcen festgelegt werden, die Aspose.Words beim Speichern eines Dokuments in HTML erstellt.

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
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


