---
title: MarkdownSaveOptions.ExportImagesAsBase64
second_title: Справочник по API Aspose.Words для .NET
description: MarkdownSaveOptions свойство. Указывает сохраняются ли изображения в формате Base64 в выходной файл. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 20
url: /ru/net/aspose.words.saving/markdownsaveoptions/exportimagesasbase64/
---
## MarkdownSaveOptions.ExportImagesAsBase64 property

Указывает, сохраняются ли изображения в формате Base64 в выходной файл. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

### Примечания

Когда для этого свойства установлено значение`истинный` данные изображений экспортируются непосредственно в **изображение** элементы и отдельные файлы не создаются.

### Примеры

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
* пространство имен [Aspose.Words.Saving](../../markdownsaveoptions/)
* сборка [Aspose.Words](../../../)


