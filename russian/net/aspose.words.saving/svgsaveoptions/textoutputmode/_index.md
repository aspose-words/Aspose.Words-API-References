---
title: SvgSaveOptions.TextOutputMode
linktitle: TextOutputMode
articleTitle: TextOutputMode
second_title: Aspose.Words для .NET
description: SvgSaveOptions TextOutputMode свойство. Получает или задает значение определяющее способ отображения текста в SVG на С#.
type: docs
weight: 90
url: /ru/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

Получает или задает значение, определяющее способ отображения текста в SVG.

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

## Примечания

Используйте это свойство, чтобы получить или установить режим отображения текста внутри документа при сохранении в формате SVG.

Значение по умолчанию:UseTargetMachineFonts.

## Примеры

Показывает, как имитировать свойства изображений при преобразовании документа .docx в .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Настройте объект SvgSaveOptions для сохранения без границ страницы и выбираемого текста.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### Смотрите также

* enum [SvgTextOutputMode](../../svgtextoutputmode/)
* class [SvgSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
