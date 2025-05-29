---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
linktitle: UseGdiRasterOperationsEmulation
articleTitle: UseGdiRasterOperationsEmulation
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MetafileRenderingOptions UseGdiRasterOperationsEmulation для оптимизации растровых операций с GDI. Повысьте производительность и гибкость сегодня!
type: docs
weight: 80
url: /ru/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

Возвращает или задает значение, определяющее, следует ли использовать GDI+ для эмуляции растровых операций.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

## Примечания

Библиотека Windows GDI+ может использоваться для эмуляции растровых операций. Она обеспечивает поддержку всех растровых операций по сравнению с собственной эмуляцией Aspose.Words, но производительность может быть ниже в некоторых случаях.

Когда это значение установлено на`истинный`Aspose.Words использует GDI+ для эмуляции растровых операций.

Когда это значение установлено на`ЛОЖЬ`Aspose.Words использует собственную реализацию эмуляции растровых операций.

Эта опция используется только в том случае, если метафайл отображается как векторная графика.

Значение по умолчанию:`ЛОЖЬ`.

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

* class [MetafileRenderingOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
