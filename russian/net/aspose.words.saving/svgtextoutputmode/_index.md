---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: Aspose.Words для .NET
description: Aspose.Words.Saving.SvgTextOutputMode перечисление. Позволяет указать как должен отображаться текст внутри документа при сохранении в формате SVG на С#.
type: docs
weight: 5610
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
| UseSvgFonts | `0` | Шрифты SVG используются для рендеринга текста. Обратите внимание: не все браузеры поддерживают шрифты SVG. |
| UseTargetMachineFonts | `1` | Шрифты, установленные на целевой машине, используются для рендеринга текста. Обратите внимание: если некоторые шрифты, используемые в документе, недоступны на целевом компьютере, документ может выглядеть иначе. |
| UsePlacedGlyphs | `2` | Текст отображается с помощью кривых. Обратите внимание, что выделение текста не будет работать, если вы используете эту опцию. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
