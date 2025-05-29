---
title: SaveOptions.UseHighQualityRendering
linktitle: UseHighQualityRendering
articleTitle: UseHighQualityRendering
second_title: Aspose.Words для .NET
description: Оптимизируйте SaveOptions с помощью свойства UseHighQualityRendering для превосходного вывода. Управляйте скоростью и качеством рендеринга для идеальных результатов.
type: docs
weight: 210
url: /ru/net/aspose.words.saving/saveoptions/usehighqualityrendering/
---
## SaveOptions.UseHighQualityRendering property

Возвращает или задает значение, определяющее, следует ли использовать высококачественные (т. е. медленные) алгоритмы рендеринга.

```csharp
public bool UseHighQualityRendering { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` .

Это свойство используется при экспорте документа в форматы изображений: Tiff ,Png ,Bmp , Jpeg ,Emf.

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
