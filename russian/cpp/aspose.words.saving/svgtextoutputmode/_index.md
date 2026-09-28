---
title: "Aspose::Words::Saving::SvgTextOutputMode перечисление"
linktitle: "SvgTextOutputMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::SvgTextOutputMode перечисление. Позволяет указать, как текст внутри документа должен рендериться при сохранении в формате SVG в C++."
type: docs
weight: 83000
url: /ru/cpp/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enum


Позволяет указать, как текст внутри документа должен отображаться при сохранении в формате SVG.

```cpp
enum class SvgTextOutputMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| UseSvgFonts | 0 | SVG шрифты используются для рендеринга текста. Примечание, не все браузеры поддерживают SVG шрифты. |
| UseTargetMachineFonts | 1 | [Fonts](../../aspose.words.fonts/) установленные на целевой машине используются для рендеринга текста. Примечание, если некоторые шрифты, используемые в документе, недоступны на целевой машине, документ может выглядеть иначе. |
| UsePlacedGlyphs | 2 | Текст рендерится с помощью кривых. Примечание, выделение текста не будет работать, если вы используете эту опцию. |


## Примеры



Показывает, как имитировать свойства изображений при конвертации документа .docx в .svg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Настройте объект SvgSaveOptions для сохранения без границ страниц и без выделяемого текста.
auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_FitToViewPort(true);
options->set_ShowPageBorder(false);
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.SaveLikeImage.svg", options);
```

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
