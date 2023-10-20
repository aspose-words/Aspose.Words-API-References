---
title: ImageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words для .NET
description: ImageSaveOptions MetafileRenderingOptions свойство. Позволяет указать как метафайлы обрабатываются при визуализации на С#.
type: docs
weight: 90
url: /ru/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

Позволяет указать, как метафайлы обрабатываются при визуализации.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

## Примечания

КогдаVector указан, Aspose.Words сначала преобразует метафайл в векторную графику, используя собственный механизм рендеринга метафайлов, а затем визуализирует графику Vector в изображение.

КогдаBitmap указан, Aspose.Words отображает метафайл непосредственно в изображение с помощью механизма рендеринга метафайлов GDI+.

Механизм рендеринга метафайлов GDI+ работает быстрее, поддерживает почти все функции метафайлов, но при низком разрешении может давать противоречивый результат по сравнению с остальной векторной графикой (особенно для текста) на странице. Механизм рендеринга метафайлов Aspose.Words дает более стабильный результат даже при низких разрешениях, но работает медленнее и может неточно отображать сложные метафайлы.

Значение по умолчанию для[`MetafileRenderingMode`](../../metafilerenderingmode/) являетсяBitmap.

## Примеры

Показывает, как установить режим рендеринга при сохранении документов с изображениями метафайлов Windows в другие форматы изображений.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(Image.FromFile(ImageDir + "Windows MetaFile.wmf"));

// Когда мы сохраняем документ как изображение, мы можем передать объект SaveOptions
// определить, как операция сохранения будет обрабатывать метафайлы Windows в документе.
// Если мы установим для свойства «RenderingMode» значение «MetafileRenderingMode.Vector»,
// или «MetafileRenderingMode.VectorWithFallback», мы будем отображать все метафайлы как векторную графику.
// Если мы установим для свойства «RenderingMode» значение «MetafileRenderingMode.Bitmap», мы будем отображать все метафайлы как растровые изображения.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// Aspose.Words использует GDI+ для эмуляции растровых операций, когда значение установлено в true.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### Смотрите также

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
