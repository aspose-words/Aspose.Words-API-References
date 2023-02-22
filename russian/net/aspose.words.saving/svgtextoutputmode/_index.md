---
title: Enum SvgTextOutputMode
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.SvgTextOutputMode перечисление. 
type: docs
weight: 5330
url: /ru/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

```csharp
public enum SvgTextOutputMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| UseSvgFonts | `0` | Шрифты SVG используются для отображения текста. Обратите внимание, что не все браузеры поддерживают шрифты SVG. |
| UseTargetMachineFonts | `1` | Шрифты, установленные на целевой машине, используются для рендеринга текста. Обратите внимание: если некоторые шрифты, используемые в документе, недоступны на целевой машине, документ может выглядеть иначе. |
| UsePlacedGlyphs | `2` | Текст визуализируется с использованием кривых. Обратите внимание: выделение текста не будет работать, если вы используете эту опцию. |

### Примеры

Показывает, как имитировать свойства изображений при преобразовании документа .docx в .svg.

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


