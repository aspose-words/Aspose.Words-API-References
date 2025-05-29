---
title: MarkdownSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words для .NET
description: Оптимизируйте экспорт Markdown с помощью свойства ImageResolution, устанавливая пользовательские выходные разрешения для более четких изображений. По умолчанию 96 точек на дюйм.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/markdownsaveoptions/imageresolution/
---
## MarkdownSaveOptions.ImageResolution property

Указывает выходное разрешение для изображений при экспорте в Markdown. Значение по умолчанию:`96 точек на дюйм` .

```csharp
public int ImageResolution { get; set; }
```

## Примеры

Показывает, как установить выходное разрешение для изображений.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ImageResolution = 300;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

### Смотрите также

* class [MarkdownSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
