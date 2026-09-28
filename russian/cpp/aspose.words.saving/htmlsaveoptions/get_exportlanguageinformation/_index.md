---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation метод"
linktitle: "get_ExportLanguageInformation"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation метод. Указывает, экспортируется ли информация о языке в HTML, MHTML или EPUB. По умолчанию false в C++."
type: docs
weight: 20000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_exportlanguageinformation/
---
## HtmlSaveOptions::get_ExportLanguageInformation method


Указывает, экспортируется ли информация о языке в HTML, MHTML или EPUB. По умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation() const
```

## Примечания


Когда это свойство установлено в **true**, Aspose.Words выводит HTML‑атрибут **lang** у элементов документа, указывающих язык. Это может потребоваться для сохранения семантики, связанной с языком.

## Примеры



Показывает, как сохранить информацию о языке при сохранении в .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Используйте построитель для записи текста с форматированием в разных локалях.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID());
builder->Writeln(u"Hello world!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-GB")->get_LCID());
builder->Writeln(u"Hello again!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU")->get_LCID());
builder->Write(u"Привет, мир!");

// При сохранении документа в HTML мы можем передать объект SaveOptions
// чтобы либо сохранить, либо отбросить локаль каждого отформатированного текста.
// Если мы установим флаг \"ExportLanguageInformation\" в значение \"true\",
// выходной HTML‑документ будет содержать локали в атрибутах \"lang\" тегов <span>.
// Если мы установим флаг \"ExportLanguageInformation\" в значение \"false',
// текст в выходном HTML‑документе не будет содержать информацию о локали.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportLanguageInformation(exportLanguageInformation);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportLanguageInformation.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"en-GB\">Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Привет, мир!</span>"));
}
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
