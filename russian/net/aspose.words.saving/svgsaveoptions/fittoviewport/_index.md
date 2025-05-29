---
title: SvgSaveOptions.FitToViewPort
linktitle: FitToViewPort
articleTitle: FitToViewPort
second_title: Aspose.Words для .NET
description: Узнайте, как свойство SvgSaveOptions FitToViewPort оптимизирует вывод SVG для идеального заполнения любого окна браузера или контейнера, обеспечивая потрясающие визуальные эффекты.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

Указывает, должен ли выходной SVG-файл заполнять доступную область просмотра (окно браузера или контейнер). Если установлено значение`истинный`Ширина и высота выходного SVG установлены на 100%.

Значение по умолчанию:`ЛОЖЬ`.

```csharp
public bool FitToViewPort { get; set; }
```

## Примеры

Показывает, как имитировать свойства изображений при конвертации документа .docx в .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Настройте объект SvgSaveOptions для сохранения без границ страницы или выбираемого текста.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### Смотрите также

* class [SvgSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
