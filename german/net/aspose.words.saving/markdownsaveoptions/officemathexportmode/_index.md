---
title: MarkdownSaveOptions.OfficeMathExportMode
linktitle: OfficeMathExportMode
articleTitle: OfficeMathExportMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „MarkdownSaveOptions OfficeMathExportMode“, um die OfficeMath-Ausgabe anzupassen. Optimieren Sie Ihre Dateien mit flexiblen Exporteinstellungen!
type: docs
weight: 120
url: /de/net/aspose.words.saving/markdownsaveoptions/officemathexportmode/
---
## MarkdownSaveOptions.OfficeMathExportMode property

Gibt an, wie OfficeMath in die Ausgabedatei geschrieben wird. Der Standardwert istText .

```csharp
public MarkdownOfficeMathExportMode OfficeMathExportMode { get; set; }
```

## Beispiele

Zeigt, wie OfficeMath in das Dokument geschrieben wird.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### Siehe auch

* enum [MarkdownOfficeMathExportMode](../../markdownofficemathexportmode/)
* class [MarkdownSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
