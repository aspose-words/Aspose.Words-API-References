---
title: PdfSaveOptions.CacheBackgroundGraphics
linktitle: CacheBackgroundGraphics
articleTitle: CacheBackgroundGraphics
second_title: Aspose.Words для .NET
description: PdfSaveOptions CacheBackgroundGraphics свойство. Получает или задает значение определяющее следует ли кэшировать графику размещенную в фоновом режиме документа на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

Получает или задает значение, определяющее, следует ли кэшировать графику, размещенную в фоновом режиме документа.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

## Примечания

Значение по умолчанию:`истинный` а фоновая графика записывается в PDF-документ как xObject.

Когда значение`ЛОЖЬ` фоновая графика не кэшируется.

Некоторые фигуры не поддерживаются для кэширования (фигуры с полями, закладками, HRefs).

Фоновая графика документа — это различные фигуры, диаграммы, изображения, размещенные в нижнем колонтитуле или заголовке, , а также фон и граница страницы.

## Примеры

Показывает, как кэшировать графику, размещенную в фоновом режиме документа.

```csharp
Document doc = new Document(MyDir + "Background images.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.CacheBackgroundGraphics = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf", saveOptions);

long asposeToPdfSize = new FileInfo(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf").Length;
long wordToPdfSize = new FileInfo(MyDir + "Background images (word to pdf).pdf").Length;

Assert.Less(asposeToPdfSize, wordToPdfSize);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
