---
title: MarkdownSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words für .NET
description: MarkdownSaveOptions ExportImagesAsBase64 eigendom. Gibt an ob Bilder im Base64Format in der Ausgabedatei gespeichert werden. Der Standardwert istFALSCH  in C#.
type: docs
weight: 20
url: /de/net/aspose.words.saving/markdownsaveoptions/exportimagesasbase64/
---
## MarkdownSaveOptions.ExportImagesAsBase64 property

Gibt an, ob Bilder im Base64-Format in der Ausgabedatei gespeichert werden. Der Standardwert ist`FALSCH` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Bemerkungen

Wenn diese Eigenschaft auf festgelegt ist`WAHR` Bilddaten werden direkt in das exportiert **Bild** Elemente und separate Dateien werden nicht erstellt.

## Beispiele

Zeigt, wie ein .md-Dokument mit darin eingebetteten Bildern gespeichert wird.

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
