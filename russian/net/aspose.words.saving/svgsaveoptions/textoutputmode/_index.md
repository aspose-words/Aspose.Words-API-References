---
title: SvgSaveOptions.TextOutputMode
linktitle: TextOutputMode
articleTitle: TextOutputMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SvgSaveOptions TextOutputMode, которое управляет рендерингом текста в SVG для улучшения визуального качества и настройки. Оптимизируйте свою графику сегодня!
type: docs
weight: 120
url: /ru/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

Возвращает или задает значение, определяющее, как текст должен отображаться в SVG.

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

## Примечания

Используйте это свойство, чтобы получить или задать режим отображения текста внутри документа при сохранении в формате SVG.

Значение по умолчанию:UseTargetMachineFonts.

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

* enum [SvgTextOutputMode](../../svgtextoutputmode/)
* class [SvgSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
