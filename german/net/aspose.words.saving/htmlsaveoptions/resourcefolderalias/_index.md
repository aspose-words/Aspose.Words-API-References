---
title: HtmlSaveOptions.ResourceFolderAlias
linktitle: ResourceFolderAlias
articleTitle: ResourceFolderAlias
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre HTML-Dokumente mit der ResourceFolderAlias-Eigenschaft von HtmlSaveOptions und definieren Sie Ordnernamen für eine effiziente URI-Erstellung von Ressourcen.
type: docs
weight: 450
url: /de/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

Gibt den Namen des Ordners an, der zum Erstellen der URIs aller in ein HTML-Dokument geschriebenen Ressourcen verwendet wird. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string ResourceFolderAlias { get; set; }
```

## Bemerkungen

`ResourceFolderAlias` ist die einfachste Möglichkeit, festzulegen, wie URIs für alle Ressourcendateien aufgebaut sein sollen. Dieselben Informationen können für Bilder und Schriftarten separat angegeben werden über[`ImagesFolderAlias`](../imagesfolderalias/) und[`FontsFolderAlias`](../fontsfolderalias/) Eigenschaften. Es gibt jedoch keine eigene Eigenschaft für CSS.

`ResourceFolderAlias` hat eine niedrigere Priorität als[`FontsFolderAlias`](../fontsfolderalias/) und[`ImagesFolderAlias`](../imagesfolderalias/) Wenn zum Beispiel beide`ResourceFolderAlias` und[`FontsFolderAlias`](../fontsfolderalias/) angegeben sind, werden die URIs der Schriftarten mit erstellt[`FontsFolderAlias`](../fontsfolderalias/) während URIs von Bildern und CSS mit erstellt werden`ResourceFolderAlias`.

Wenn`ResourceFolderAlias` ist leer, der[`ResourceFolder`](../resourcefolder/) Der Eigenschaftswert wird zum Erstellen von Ressourcen-URIs verwendet .

Wenn`ResourceFolderAlias` auf „.“ (Punkt) gesetzt ist, enthalten Ressourcen-URIs nur Dateinamen ohne Pfad.

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
