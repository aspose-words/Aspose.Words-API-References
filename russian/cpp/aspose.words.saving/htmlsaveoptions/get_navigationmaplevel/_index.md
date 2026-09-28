---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel метод"
linktitle: "get_NavigationMapLevel"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel метод. Указывает максимальный уровень заголовков, включаемых в карту навигации при экспорте в форматы EPUB, MOBI или AZW3. Значение по умолчанию — %3 в C++."
type: docs
weight: 40500
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_navigationmaplevel/
---
## HtmlSaveOptions::get_NavigationMapLevel method


Указывает максимальный уровень заголовков, включаемых в навигационную карту при экспорте в форматы EPUB, MOBI или AZW3. Значение по умолчанию **%3**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel() const
```

## Примечания


Карта навигации позволяет пользовательским агентам обеспечить простой способ перемещения по структуре документа. Обычно точки навигации соответствуют заголовкам в документе. Чтобы заполнить заголовки до уровня **N**, присвойте это значение свойству [NavigationMapLevel](./).

По умолчанию заполняются три уровня заголовков: абзацы стилей **Heading 1**, **Heading 2** и **Heading 3**. Вы можете установить это свойство в значение от 1 до 9, чтобы запросить соответствующий максимальный уровень. Установка в ноль сократит карту навигации только до корня документа или корней частей документа.

## Примеры



Показывает, как создать оглавление для документов Azw3.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Azw3);
options->set_NavigationMapLevel(2);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```


Показывает, как создать оглавление для документов Mobi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mobi);
options->set_NavigationMapLevel(5);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateMobiToc.mobi", options);
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
