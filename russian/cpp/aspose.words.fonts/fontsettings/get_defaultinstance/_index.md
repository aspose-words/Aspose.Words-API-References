---
title: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance метод"
linktitle: "get_DefaultInstance"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontSettings::get_DefaultInstance метод. Статические настройки шрифта по умолчанию в C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.fonts/fontsettings/get_defaultinstance/
---
## FontSettings::get_DefaultInstance method


Статические параметры шрифтов по умолчанию.

```cpp
static System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Fonts::FontSettings::get_DefaultInstance()
```


## Примеры



Показывает, как настроить экземпляр настроек шрифта по умолчанию.
```cpp
// Настройте экземпляр настроек шрифта по умолчанию для использования шрифта "Courier New"
// в качестве резервной замены, когда мы пытаемся использовать неизвестный шрифт.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->get_Enabled());

auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

// У этого документа нет конфигурации FontSettings. При рендеринге документа,
// экземпляр FontSettings по умолчанию разрешит отсутствующий шрифт.
// Aspose.Words будет использовать "Courier New" для рендеринга текста, использующего неизвестный шрифт.
ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontSettings()));

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontInstance.pdf");
```

## См. также

* Class [FontSettings](../)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
