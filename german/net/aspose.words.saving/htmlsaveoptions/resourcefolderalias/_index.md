---
title: HtmlSaveOptions.ResourceFolderAlias
linktitle: ResourceFolderAlias
articleTitle: ResourceFolderAlias
second_title: Aspose.Words für .NET
description: HtmlSaveOptions ResourceFolderAlias eigendom. Gibt den Namen des Ordners an der zum Erstellen der URIs aller in ein HTMLDokument geschriebenen Ressourcen verwendet wird. Der Standardwert ist eine leere Zeichenfolge in C#.
type: docs
weight: 430
url: /de/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

Gibt den Namen des Ordners an, der zum Erstellen der URIs aller in ein HTML-Dokument geschriebenen Ressourcen verwendet wird. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string ResourceFolderAlias { get; set; }
```

## Bemerkungen

`ResourceFolderAlias` ist die einfachste Möglichkeit, anzugeben, wie URIs für alle Ressourcendateien erstellt werden sollen. Dieselben Informationen können für Bilder und Schriftarten separat angegeben werden über[`ImagesFolderAlias`](../imagesfolderalias/) und[`FontsFolderAlias`](../fontsfolderalias/) Eigenschaften bzw. Es gibt jedoch keine individuelle Eigenschaft für CSS.

`ResourceFolderAlias` hat niedrigere Priorität als[`FontsFolderAlias`](../fontsfolderalias/) und[`ImagesFolderAlias`](../imagesfolderalias/) . Wenn zum Beispiel beides`ResourceFolderAlias` und[`FontsFolderAlias`](../fontsfolderalias/) angegeben sind, werden die URIs der Schriftarten mit erstellt.[`FontsFolderAlias`](../fontsfolderalias/) , während URIs von Bildern und CSS mit erstellt werden`ResourceFolderAlias`.

Wenn`ResourceFolderAlias` ist leer, die[`ResourceFolder`](../resourcefolder/)Der Eigenschaftswert wird verwendet , um Ressourcen-URIs zu erstellen.

Wenn`ResourceFolderAlias` ist eingestellt auf '.' (Punkt), Ressourcen-URIs enthalten nur Dateinamen, ohne einen Pfad.

## Beispiele

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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
