---
title: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode метод"
linktitle: "get_TextOutputMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode метод. Получает или задает значение, определяющее, как текст должен отображаться в SVG в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.saving/svgsaveoptions/get_textoutputmode/
---
## SvgSaveOptions::get_TextOutputMode method


Получает или задает значение, определяющее, как текст должен отображаться в SVG.

```cpp
Aspose::Words::Saving::SvgTextOutputMode Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode() const
```

## Примечания


Используйте это свойство, чтобы получить или задать режим отображения текста внутри документа при сохранении в формате SVG.

Значение по умолчанию — [UseTargetMachineFonts](../../svgtextoutputmode/).

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

* Enum [SvgTextOutputMode](../../svgtextoutputmode/)
* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
