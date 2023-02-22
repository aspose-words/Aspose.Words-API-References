---
title: HtmlSaveOptions.FontsFolderAlias
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt den Namen des Ordners an der zum Erstellen von SchriftartURIs verwendet wird die in ein HTMLDokument geschrieben werden. Standard ist eine leere Zeichenfolge.
type: docs
weight: 330
url: /de/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

Gibt den Namen des Ordners an, der zum Erstellen von Schriftart-URIs verwendet wird, die in ein HTML-Dokument geschrieben werden. Standard ist eine leere Zeichenfolge.

```csharp
public string FontsFolderAlias { get; set; }
```

### Bemerkungen

Beim Speichern von a[`Document`](../../../aspose.words/document/) im HTML-Format u[`ExportFontResources`](../exportfontresources/) ist eingestellt auf`Stimmt` , muss Aspose.Words im Dokument verwendete Schriftarten als eigenständige Dateien speichern. [`FontsFolder`](../fontsfolder/) können Sie angeben, wo die Schriftarten gespeichert werden und `FontsFolderAlias` ermöglicht die Angabe, wie die Schrift-URIs aufgebaut werden.

Wenn`FontsFolderAlias` kein leerer String ist, dann wird die Font-URI in HTML geschrieben FontsFolderAlias + &lt;Name der Schriftartdatei&gt;.

Wenn`FontsFolderAlias` ein leerer String ist, dann wird der Font-URI in HTML geschriebenFontsFolder + &lt;Name der Schriftartdatei&gt;.

Wenn`FontsFolderAlias`ist eingestellt auf '.' (Punkt), dann wird der Schriftartdateiname unabhängig von anderen Optionen ohne Pfad in HTML geschrieben.

Eine alternative Möglichkeit, den Namen des Ordners zum Erstellen von Schriftart-URIs anzugeben, ist die Verwendung[`ResourceFolderAlias`](../resourcefolderalias/).

### Beispiele

Zeigt, wie Ordner und Ordneraliase für extern gespeicherte Ressourcen festgelegt werden, die Aspose.Words erstellt, wenn ein Dokument in HTML gespeichert wird.

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


