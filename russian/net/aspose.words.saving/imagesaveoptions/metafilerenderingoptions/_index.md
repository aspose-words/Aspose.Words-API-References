---
title: ImageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImageSaveOptions MetafileRenderingOptions, позволяющее управлять обработкой метафайлов в визуализированном выводе для повышения качества изображения.
type: docs
weight: 90
url: /ru/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

Позволяет указать, как метафайлы обрабатываются в визуализированном выводе.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

## Примечания

КогдаVector указан, Aspose.Words сначала преобразует метафайл в векторную графику, используя собственный механизм рендеринга метафайлов, а затем преобразует графику vector в изображение.

КогдаBitmap если указано, Aspose.Words визуализирует метафайл x000d_ непосредственно в изображение, используя механизм визуализации метафайлов GDI+.

Механизм рендеринга метафайлов GDI+ работает быстрее, поддерживает почти все функции метафайлов, но на низких разрешениях может давать нестабильный результат по сравнению с остальной векторной графикой (особенно для текста) на странице. Механизм рендеринга метафайлов Aspose.Words даст более стабильный результат даже на низких разрешениях, но работает медленнее и может неточно отображать сложные метафайлы.

Значение по умолчанию для[`MetafileRenderingMode`](../../metafilerenderingmode/) являетсяBitmap.

## Примеры

Показывает, как установить режим рендеринга при сохранении документов с изображениями Windows Metafile в других форматах изображений.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Windows MetaFile.wmf");

// Когда мы сохраняем документ как изображение, мы можем передать объект SaveOptions
// определить, как операция сохранения будет обрабатывать метафайлы Windows в документе.
// Если мы установим свойство "RenderingMode" на "MetafileRenderingMode.Vector",
// или "MetafileRenderingMode.VectorWithFallback", мы будем визуализировать все метафайлы как векторную графику.
// Если мы установим свойство "RenderingMode" на "MetafileRenderingMode.Bitmap", мы будем визуализировать все метафайлы как растровые изображения.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// Aspose.Words использует GDI+ для эмуляции растровых операций, если задано значение true.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### Смотрите также

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
