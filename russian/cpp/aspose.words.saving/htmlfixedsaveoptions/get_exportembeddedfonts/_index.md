---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts метод"
linktitle: "get_ExportEmbeddedFonts"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts метод. Указывает, должны ли шрифты быть встроены в документ Html в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного файла Html в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedfonts/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedFonts method


Указывает, следует ли внедрять шрифты в документ Html в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного файла Html.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts() const
```


## Примеры



Показывает, как определить, где хранить встроенные шрифты при экспорте документа в Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

// Когда мы экспортируем документ со встроенными шрифтами в .html,
// Aspose.Words может разместить шрифты в двух возможных местах.
// Установка флага "ExportEmbeddedFonts" в значение "true" сохранит необработанные данные встроенных шрифтов внутри таблицы стилей CSS,
// в свойстве "url" правила "@font-face". Это может создать огромный файл таблицы стилей CSS
// и уменьшить количество внешних файлов, которые создаст эта HTML‑конверсия.
// Установка этого флага в "false" создаст файл для каждого шрифта.
// CSS‑таблица стилей будет ссылаться на каждый файл шрифта, используя свойство "url" правила "@font-face".
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedFonts(exportEmbeddedFonts);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(0, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(2, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
```

## См. также

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
