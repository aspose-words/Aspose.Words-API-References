---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames метод"
linktitle: "get_ResolveFontNames"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames метод. Указывает, разрешаются ли имена семейств шрифтов, используемых в документе, и заменяются ли они согласно FontSettings при записи в форматы на основе HTML в C++."
type: docs
weight: 42000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_resolvefontnames/
---
## HtmlSaveOptions::get_ResolveFontNames method


Указывает, разрешаются ли имена семейств шрифтов, используемых в документе, и заменяются ли они согласно [FontSettings](../../../aspose.words/document/get_fontsettings/) при записи в форматы на основе HTML.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames() const
```

## Примечания


По умолчанию эта опция установлена в **false**, и имена семейств шрифтов записываются в HTML как указано в исходных документах. То есть [FontSettings](../../../aspose.words/document/get_fontsettings/) игнорируются и разрешение или замена имен семейств шрифтов не выполняются.

Если эта опция установлена в **true**, Aspose.Words использует [FontSettings](../../../aspose.words/document/get_fontsettings/) для разрешения каждого имени семейства шрифтов, указанного в исходном документе, в имя доступного семейства шрифтов, выполняя замену шрифтов при необходимости.

## Примеры



Показывает, как разрешить все имена шрифтов перед их записью в HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Этот документ содержит текст, в котором упоминается шрифт, которого у нас нет.
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"28 Days Later")));

// Если у нас нет возможности получить этот шрифт, и мы хотим иметь возможность отобразить весь текст
// в этом документе в выходном HTML, мы можем заменить его другим шрифтом.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_Enabled(true);

doc->set_FontSettings(fontSettings);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
// По умолчанию эта опция установлена в 'False' и Aspose.Words записывает имена шрифтов так, как указано в исходном документе
saveOptions->set_ResolveFontNames(resolveFontNames);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html");

ASSERT_TRUE(resolveFontNames ? System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:Arial\">")->get_Success() : System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:\'28 Days Later\'\">")->get_Success());
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
