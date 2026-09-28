---
title: "Метод Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort"
linktitle: "get_FitToViewPort"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort. Указывает, должен ли результирующий SVG заполнять доступную область просмотра (окно браузера или контейнер). При установке в true ширина и высота выходного SVG задаются в 100%. Значение по умолчанию — false в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/svgsaveoptions/get_fittoviewport/
---
## SvgSaveOptions::get_FitToViewPort method


Указывает, должен ли выходной SVG заполнять доступную область области просмотра (окно браузера или контейнер). При установке в **true** ширина и высота выходного SVG устанавливаются в 100 %. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort() const
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
