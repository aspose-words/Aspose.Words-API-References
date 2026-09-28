---
title: "Aspose::Words::Document::get_FontSettings метод"
linktitle: "get_FontSettings"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::get_FontSettings метод. Получает или задает настройки шрифтов документа в C++."
type: docs
weight: 25000
url: /ru/cpp/aspose.words/document/get_fontsettings/
---
## Document::get_FontSettings method


Получает или задает настройки шрифтов документа.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Document::get_FontSettings() const
```

## Примечания


Это свойство позволяет задавать настройки шрифтов для каждого документа. Если установить в **null**, будут использованы настройки шрифтов по умолчанию [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/).

Значение по умолчанию — **null**.

## Примеры



Показывает, как задать правила замены шрифтов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// Источник шрифтов по умолчанию содержит первый шрифт, используемый в документе.
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// Второй шрифт, \"Amethysta\", недоступен.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Мы можем настроить таблицу замены шрифтов, которая определяет
// какие шрифты Aspose.Words будет использовать в качестве замен для недоступных шрифтов.
// Установите два заменяющих шрифта для \"Amethysta\": \"Arvo\" и \"Courier New\".
// Если первый заменяющий шрифт недоступен, Aspose.Words пытается использовать второй заменяющий шрифт и так далее.
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->SetSubstitutes(u"Amethysta", System::MakeArray<System::String>({u"Arvo", u"Courier New"}));

// \"Amethysta\" недоступен, и правило замены указывает, что первым шрифтом‑заменой будет \"Arvo\".
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// \"Arvo\" также недоступен, но \"Courier New\" доступен.
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// Выходной документ отобразит текст, использующий шрифт \"Amethysta\", отформатированный шрифтом \"Courier New\".
doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitution.pdf");
```

## См. также

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
