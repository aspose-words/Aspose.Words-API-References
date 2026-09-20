---
title: "Метод Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder"
linktitle: "get_ShowPageBorder"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder. Управляет тем, добавляется ли граница к контуру страницы. По умолчанию true в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.saving/svgsaveoptions/get_showpageborder/
---
## SvgSaveOptions::get_ShowPageBorder method


Управляет тем, добавляется ли граница к контуру страницы. По умолчанию **true**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder() const
```


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

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
