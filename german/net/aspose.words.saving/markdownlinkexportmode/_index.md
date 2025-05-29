---
title: MarkdownLinkExportMode Enum
linktitle: MarkdownLinkExportMode
articleTitle: MarkdownLinkExportMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Aufzählung Aspose.Words MarkdownLinkExportMode den Linkexport in Markdown verbessert und Ihren Dokumentkonvertierungsprozess mühelos optimiert.
type: docs
weight: 6030
url: /de/net/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enumeration

Gibt an, wie Links in Markdown exportiert werden.

```csharp
public enum MarkdownLinkExportMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Auto | `0` | Exportmodus für jeden Link automatisch erkennen. |
| Inline | `1` | Alle Links als Inline-Blöcke exportieren. |
| Reference | `2` | Alle Links als Referenzblöcke exportieren. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
