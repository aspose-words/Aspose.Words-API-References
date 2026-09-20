---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method"
linktitle: "get_FontResourcesSubsettingSizeThreshold"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method. Управляет тем, какие ресурсы шрифтов требуют субсеттинга при сохранении в HTML, MHTML или EPUB. По умолчанию — %0 в C++."
type: docs
weight: 31000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method


Управляет тем, какие ресурсы шрифтов требуют субсеттинга при сохранении в HTML, MHTML или EPUB. По умолчанию **%0**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold() const
```

## Примечания


[ExportFontResources](../get_exportfontresources/) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. [Font](../../../aspose.words/font/) subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

[Font](../../../aspose.words/font/) subsetting works as follows:

* By default, all exported fonts are subsetted.
* Setting [FontResourcesSubsettingSizeThreshold](./) to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
* Setting the property to **MaxValue** suppresses font subsetting.



**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## Примеры



Показывает, как работать с субсеттингом шрифтов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Courier New");
builder->Writeln(u"Hello world!");

// При сохранении документа в HTML мы можем передать объект SaveOptions, чтобы настроить субсеттинг шрифтов.
// Предположим, мы устанавливаем флаг "ExportFontResources" в значение "true" и также указываем папку в свойстве "FontsFolder".
// В этом случае операция сохранения создаст эту папку и поместит в неё файл .ttf
// в эту папку для каждого шрифта, используемого в нашем документе.
// Каждый файл .ttf будет содержать полный набор глифов данного шрифта,
// что может привести к очень большому файлу, сопровождающему документ.
// Когда мы применяем субсеттинг к шрифту, его экспортированные необработанные данные будут содержать только глифы, которые документ
// использует, вместо полного набора глифов. Если текст в нашем документе использует лишь небольшую часть шрифта
// набор глифов, то субсеттинг значительно уменьшит размер наших выходных документов.
// Мы можем использовать свойство "FontResourcesSubsettingSizeThreshold", чтобы задать размер файла .ttf в байтах.
// Если экспортированный шрифт создаёт файл большего размера, чем указано, то операция сохранения применит субсеттинг к этому шрифту.
// Установка порога 0 применяет субсеттинг ко всем шрифтам,
// и установка его в "int.MaxValue" эффективно отключает субсеттинг.
System::String fontsFolder = get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.Fonts";

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontResources(true);
options->set_FontsFolder(fontsFolder);
options->set_FontResourcesSubsettingSizeThreshold(fontResourcesSubsettingSizeThreshold);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.html", options);

System::ArrayPtr<System::String> fontFileNames = System::IO::Directory::GetFiles(fontsFolder)->LINQ_Where(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String s)>>([](System::String s) -> bool
{
    return s.EndsWith(u".ttf");
})))->LINQ_ToArray();

ASSERT_EQ(3, fontFileNames->get_Length());

for (System::String filename : fontFileNames)
{
    // По умолчанию файлы .ttf для каждого из наших трёх шрифтов будут превышать 700 МБ.
    // Субсеттинг уменьшит их все до менее чем 30 МБ.
    auto fontFileInfo = System::MakeObject<System::IO::FileInfo>(filename);

    ASSERT_TRUE(fontFileInfo->get_Length() > 700000 || fontFileInfo->get_Length() < 30000);
    ASSERT_TRUE(System::Math::Max(fontResourcesSubsettingSizeThreshold, 30000) > System::MakeObject<System::IO::FileInfo>(filename)->get_Length());
}
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
