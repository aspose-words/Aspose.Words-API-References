---
title: "Aspose::Words::Loading::LoadOptions::get_FontSettings метод"
linktitle: "get_FontSettings"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::LoadOptions::get_FontSettings метод. Позволяет задавать параметры шрифтов документа в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.loading/loadoptions/get_fontsettings/
---
## LoadOptions::get_FontSettings method


Позволяет задавать параметры шрифтов документа.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Loading::LoadOptions::get_FontSettings() const
```

## Примечания


При загрузке некоторых форматов Aspose.Words может потребоваться разрешить шрифты. Например, при загрузке HTML‑документов [Aspose.Words](../../../aspose.words/) может выполнять разрешение шрифтов для обеспечения резервирования шрифтов.

Если установлено в **null**, будут использованы настройки статических шрифтов по умолчанию [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/).

Значение по умолчанию — **null**.

## Примеры



Показывает, как назначать замену шрифтов при загрузке.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// Установите правило замены шрифта для объекта LoadOptions.
// Если документ, который мы загружаем, использует шрифт, которого у нас нет,
// это правило заменит недоступный шрифт на существующий.
// В этом случае все использования "MissingFont" будут преобразованы в "Comic Sans MS".
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> substitutionRule = loadOptions->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution();
substitutionRule->AddSubstitutes(u"MissingFont", System::MakeArray<System::String>({u"Comic Sans MS"}));

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.html", loadOptions);

// На данном этапе такой текст всё ещё будет находиться в "MissingFont".
// Подстановка шрифтов будет происходить при рендеринге документа.
ASSERT_EQ(u"MissingFont", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());

doc->Save(get_ArtifactsDir() + u"FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```


Показывает, как применить настройки подстановки шрифтов при загрузке документа.
```cpp
// Создайте объект FontSettings, который заменит шрифт "Times New Roman"
// шрифтом "Arvo" из нашей папки "MyFonts".
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));

// Установите этот объект FontSettings в качестве свойства вновь созданного объекта LoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(fontSettings);

// Загрузите документ, затем отрендерите его в PDF с подстановкой шрифтов.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.FontSettings.pdf");
```

## См. также

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
