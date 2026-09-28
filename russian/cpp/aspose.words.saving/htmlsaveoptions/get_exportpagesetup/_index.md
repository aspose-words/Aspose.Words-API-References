---
title: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup"
linktitle: "get_ExportPageSetup"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup. Указывает, экспортируется ли настройка страницы в HTML, MHTML или EPUB. По умолчанию false в C++."
type: docs
weight: 24000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagesetup/
---
## HtmlSaveOptions::get_ExportPageSetup method


Указывает, экспортируется ли настройка страницы в HTML, MHTML или EPUB. По умолчанию **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup() const
```

## Примечания


Каждый [Section](../../../aspose.words/section/) в модели документа Aspose.Words предоставляет информацию о настройке страницы через класс [PageSetup](../../../aspose.words/pagesetup/). При экспорте документа в формат HTML вам может потребоваться сохранить эту информацию для дальнейшего использования. В частности, настройка страницы может быть важна для рендеринга в постраничных носителях (печать) или последующего преобразования в собственные форматы файлов Microsoft Word (DOCX, DOC, RTF, WML).

В большинстве случаев HTML предназначен для просмотра в браузерах, где пагинация не выполняется. Поэтому эта функция по умолчанию отключена.

## Примеры



Показывает, как решить, сохранять ли структуру разделов/информацию о настройке страницы при сохранении в HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TopMargin(36.0);
pageSetup->set_BottomMargin(36.0);
pageSetup->set_PaperSize(Aspose::Words::PaperSize::A5);

// При сохранении документа в HTML мы можем передать объект SaveOptions
// чтобы решить, сохранять или отбрасывать настройки страницы.
// Если установить флаг "ExportPageSetup" в значение "true", результирующий HTML‑документ будет содержать нашу конфигурацию настройки страницы.
// Если установить флаг "ExportPageSetup" в значение "false", операция сохранения отбрасывает наши настройки страницы
// для первого раздела, и оба раздела будут выглядеть одинаково.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageSetup(exportPageSetup);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageSetup.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<style type=\"text/css\">") + u"@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" + u"@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" + u"div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" + u"</style>"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<div class=\"Section_1\">") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<div>") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
