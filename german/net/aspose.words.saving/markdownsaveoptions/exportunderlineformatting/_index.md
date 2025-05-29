---
title: MarkdownSaveOptions.ExportUnderlineFormatting
linktitle: ExportUnderlineFormatting
articleTitle: ExportUnderlineFormatting
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „MarkdownSaveOptions ExportUnderlineFormatting“ Ihren Textexport verbessert. Steuern Sie die Unterstreichungsformatierung ganz einfach mit dieser booleschen Einstellung.
type: docs
weight: 50
url: /de/net/aspose.words.saving/markdownsaveoptions/exportunderlineformatting/
---
## MarkdownSaveOptions.ExportUnderlineFormatting property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob die Unterstreichungstextformatierung als Folge von zwei Pluszeichen "++" exportiert werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool ExportUnderlineFormatting { get; set; }
```

## Beispiele

Zeigt, wie Unterstreichungsformatierungen als ++ exportiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Single;
builder.Write("Lorem ipsum. Dolor sit amet.");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions() { ExportUnderlineFormatting = true };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

### Siehe auch

* class [MarkdownSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
