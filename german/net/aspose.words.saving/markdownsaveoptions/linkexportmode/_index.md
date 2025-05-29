---
title: MarkdownSaveOptions.LinkExportMode
linktitle: LinkExportMode
articleTitle: LinkExportMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die MarkdownSaveOptions LinkExportMode-Eigenschaft zur Steuerung der Linkformatierung in Ausgabedateien. Optimieren Sie Ihre Dokumentexporte mühelos!
type: docs
weight: 100
url: /de/net/aspose.words.saving/markdownsaveoptions/linkexportmode/
---
## MarkdownSaveOptions.LinkExportMode property

Gibt an, wie Links in die Ausgabedatei geschrieben werden. Der Standardwert istAuto .

```csharp
public MarkdownLinkExportMode LinkExportMode { get; set; }
```

## Beispiele

Zeigt, wie Links in die MD-Datei geschrieben werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertShape(ShapeType.Balloon, 100, 100);

// Bild wird als Referenz geschrieben:
// ![ref1]
//
// [ref1]: aw_ref.001.png
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.LinkExportMode = MarkdownLinkExportMode.Reference;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// Bild wird als Inline geschrieben:
// ![](aw_inline.001.png)
saveOptions.LinkExportMode = MarkdownLinkExportMode.Inline;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

### Siehe auch

* enum [MarkdownLinkExportMode](../../markdownlinkexportmode/)
* class [MarkdownSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
