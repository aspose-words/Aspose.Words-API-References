---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Saving.SvgTextOutputMode для настройки рендеринга текста в формате SVG, улучшения представления документа и визуальной привлекательности.
type: docs
weight: 6410
url: /ru/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

Позволяет указать, как должен отображаться текст внутри документа при сохранении в формате SVG.

```csharp
public enum SvgTextOutputMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| UseSvgFonts | `0` | Шрифты SVG используются для рендеринга текста. Обратите внимание, что не все браузеры поддерживают шрифты SVG. |
| UseTargetMachineFonts | `1` | Для отображения текста используются шрифты, установленные на целевой машине. Обратите внимание: если некоторые из шрифтов, используемых в документе, недоступны на целевой машине, документ может выглядеть иначе. |
| UsePlacedGlyphs | `2` | Текст визуализируется с использованием кривых. Обратите внимание, выделение текста не будет работать, если вы используете эту опцию. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
