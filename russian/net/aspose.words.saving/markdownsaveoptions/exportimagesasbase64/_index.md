---
title: MarkdownSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words для .NET
description: Узнайте, как свойство MarkdownSaveOptions ExportImagesAsBase64 улучшает ваши выходные файлы, позволяя сохранять изображения в формате Base64. По умолчанию — false.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/markdownsaveoptions/exportimagesasbase64/
---
## MarkdownSaveOptions.ExportImagesAsBase64 property

Указывает, сохраняются ли изображения в формате Base64 в выходном файле. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Примечания

Когда это свойство установлено в`истинный` Данные изображений экспортируются непосредственно в**имг** элементы и отдельные файлы не создаются.

## Примеры

Показывает, как сохранить документ .md со встроенными в него изображениями.

```csharp
Document doc = new Document(MyDir + "Images.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions { ExportImagesAsBase64 = exportImagesAsBase64 };

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("data:image/jpeg;base64")
    : outDocContents.Contains("MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

### Смотрите также

* class [MarkdownSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
