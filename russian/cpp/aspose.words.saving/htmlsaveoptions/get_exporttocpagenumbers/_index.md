---
title: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers"
linktitle: "get_ExportTocPageNumbers"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers. Указывает, следует ли записывать номера страниц в оглавление при сохранении в HTML, MHTML и EPUB. Значение по умолчанию — false в C++."
type: docs
weight: 29000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_exporttocpagenumbers/
---
## HtmlSaveOptions::get_ExportTocPageNumbers method


Указывает, следует ли записывать номера страниц в оглавление при сохранении в HTML, MHTML и EPUB. Значение по умолчанию **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers() const
```


## Примеры



Показывает, как отображать номера страниц при сохранении документа с оглавлением в .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте оглавление, а затем заполните документ абзацами, отформатированными с помощью стиля "Heading"
// стиль, который оглавление воспримет как элементы. Каждый элемент будет отображать абзац заголовка слева,
// и номер страницы, содержащей заголовок, справа.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 1");
builder->Writeln(u"Entry 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 3");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 4");
fieldToc->UpdatePageNumbers();
doc->UpdateFields();

// HTML‑документы не имеют страниц. Если мы сохраняем этот документ в HTML,
// номера страниц, отображаемые в нашем оглавлении, не будут иметь смысла.
// При сохранении документа в HTML мы можем передать объект SaveOptions, чтобы исключить эти номера страниц из оглавления.
// Если мы установим флаг "ExportTocPageNumbers" в значение "true",
// каждый элемент оглавления будет отображать заголовок, разделитель и номер страницы, сохраняя внешний вид, как в Microsoft Word.
// Если мы установим флаг "ExportTocPageNumbers" в значение "false",
// операция сохранения опустит как разделитель, так и номер страницы, оставив заголовок каждого элемента без изменений.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportTocPageNumbers(exportTocPageNumbers);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span>Entry 1</span>") + u"<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " + u"-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" + u"<span>2</span>" + u"</p>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<span>Entry 2</span>" + u"</p>"));
}
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
