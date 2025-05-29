---
title: MarkdownOfficeMathExportMode Enum
linktitle: MarkdownOfficeMathExportMode
articleTitle: MarkdownOfficeMathExportMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Aspose.Words.Saving.MarkdownOfficeMathExportMode den OfficeMath-Export nach Markdown verbessert und so eine genaue und effiziente Dokumentkonvertierung gewährleistet.
type: docs
weight: 6050
url: /de/net/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enumeration

Gibt an, wie Aspose.Words OfficeMath nach Markdown exportiert.

```csharp
public enum MarkdownOfficeMathExportMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Text | `0` | OfficeMath als einfachen Text exportieren. |
| Image | `1` | OfficeMath als Bild exportieren. |
| MathML | `2` | OfficeMath als MathML exportieren. |

## Beispiele

Zeigt, wie OfficeMath in das Dokument geschrieben wird.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
