---
title: SaveOptions.UseAntiAliasing
linktitle: UseAntiAliasing
articleTitle: UseAntiAliasing
second_title: Aspose.Words для .NET
description: SaveOptions UseAntiAliasing свойство. Получает или задает значение определяющее использовать ли сглаживание для рендеринга на С#.
type: docs
weight: 190
url: /ru/net/aspose.words.saving/saveoptions/useantialiasing/
---
## SaveOptions.UseAntiAliasing property

Получает или задает значение, определяющее, использовать ли сглаживание для рендеринга.

```csharp
public bool UseAntiAliasing { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` . Когда это значение установлено на`истинный` для рендеринга используется сглаживание is .

Это свойство используется при экспорте документа в следующие форматы: Tiff ,Png ,Bmp , Jpeg ,Emf . Когда документ экспортируется в the Html ,Mhtml , Epub ,Azw3 илиMobi форматы: эта опция используется для растровых изображений.

## Примеры

Показывает, как улучшить качество визуализированного документа с помощью SaveOptions.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
