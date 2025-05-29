---
title: MarkdownSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Markdown-Exporte mit der Eigenschaft „ImageResolution“ und legen Sie benutzerdefinierte Ausgabeauflösungen für schärfere Bilder fest. Standardmäßig 96 dpi.
type: docs
weight: 60
url: /de/net/aspose.words.saving/markdownsaveoptions/imageresolution/
---
## MarkdownSaveOptions.ImageResolution property

Gibt die Ausgabeauflösung für Bilder beim Exportieren nach Markdown an. Standard ist`96 dpi` .

```csharp
public int ImageResolution { get; set; }
```

## Beispiele

Zeigt, wie die Ausgabeauflösung für Bilder eingestellt wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ImageResolution = 300;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

### Siehe auch

* class [MarkdownSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
