---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
linktitle: UseGdiRasterOperationsEmulation
articleTitle: UseGdiRasterOperationsEmulation
second_title: Aspose.Words для .NET
description: MetafileRenderingOptions UseGdiRasterOperationsEmulation свойство. Получает или задает значение определяющее использовать ли GDI для эмуляции растровых операций на С#.
type: docs
weight: 80
url: /ru/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

Получает или задает значение, определяющее, использовать ли GDI+ для эмуляции растровых операций.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

## Примечания

Библиотеку Windows GDI+ можно использовать для эмуляции растровых операций. Он обеспечивает поддержку всех растровых операций по сравнению с собственной эмуляцией Aspose.Words, но в некоторых случаях производительность может быть ниже.

Когда это значение установлено на`истинный`, Aspose.Words использует GDI+ для эмуляции растровых операций.

Когда это значение установлено на`ЛОЖЬ`, Aspose.Words использует собственную реализацию эмуляции растровых операций.

Этот параметр используется только в том случае, если метафайл отображается как векторная графика.

Значение по умолчанию:`ЛОЖЬ`.

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

* class [MetafileRenderingOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
