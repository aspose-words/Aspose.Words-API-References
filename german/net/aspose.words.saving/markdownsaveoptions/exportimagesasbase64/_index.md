---
title: MarkdownSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „MarkdownSaveOptions ExportImagesAsBase64“ Ihre Ausgabedateien verbessert, indem sie das Speichern von Bildern im Base64-Format ermöglicht. Standardmäßig „false“.
type: docs
weight: 40
url: /de/net/aspose.words.saving/markdownsaveoptions/exportimagesasbase64/
---
## MarkdownSaveOptions.ExportImagesAsBase64 property

Gibt an, ob Bilder im Base64-Format in der Ausgabedatei gespeichert werden. Der Standardwert ist`FALSCH` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Bemerkungen

Wenn diese Eigenschaft auf`WAHR` Bilddaten werden direkt in die**img** Elemente und separate Dateien werden nicht erstellt.

## Beispiele

Zeigt, wie ein MD-Dokument mit eingebetteten Bildern gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Images.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions { ExportImagesAsBase64 = exportImagesAsBase64 };

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("data:image/jpeg;base64")
    : outDocContents.Contains("MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

### Siehe auch

* class [MarkdownSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
