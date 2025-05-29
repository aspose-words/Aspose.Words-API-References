---
title: PdfSaveOptions.CacheBackgroundGraphics
linktitle: CacheBackgroundGraphics
articleTitle: CacheBackgroundGraphics
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PdfSaveOptions CacheBackgroundGraphics, которое оптимизирует кэширование графики документа, улучшая создание PDF-файлов и производительность.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

Возвращает или задает значение, определяющее, следует ли кэшировать графику, размещенную в фоне документа.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

## Примечания

Значение по умолчанию:`истинный` и фоновая графика записываются в PDF-документ как xObject.

Когда значение равно`ЛОЖЬ` фоновая графика не кэшируется.

Некоторые фигуры не поддерживаются для кэширования (фигуры с полями, закладками, HRef).

Фоновая графика документа — это различные фигуры, диаграммы, изображения, размещаемые в нижнем или верхнем колонтитуле, , а также фон и граница страницы.

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
