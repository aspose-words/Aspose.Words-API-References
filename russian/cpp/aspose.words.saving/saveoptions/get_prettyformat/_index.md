---
title: "метод Aspose::Words::Saving::SaveOptions::get_PrettyFormat"
linktitle: "get_PrettyFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::SaveOptions::get_PrettyFormat метод. Когда true, красиво форматирует вывод, где это применимо. Значение по умолчанию — false в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.saving/saveoptions/get_prettyformat/
---
## SaveOptions::get_PrettyFormat method


Когда **true**, вывод форматируется красиво, где это применимо. Значение по умолчанию **false**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_PrettyFormat() const
```

## Примечания


Установите значение **true**, чтобы сделать вывод HTML, MHTML, EPUB, WordML, RTF, DOCX и ODT читаемым для человека. Полезно для тестирования или отладки.

## Примеры



Показывает, как улучшить читаемость исходного кода сохранённого .html‑документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto htmlOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
htmlOptions->set_PrettyFormat(usePrettyFormat);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.PrettyFormat.html", htmlOptions);

// Включение красивого формата делает исходный HTML‑код более читаемым за счёт добавления табуляций и символов новой строки.
System::String html = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.PrettyFormat.html");

System::String newLine = System::Environment::get_NewLine();
if (usePrettyFormat)
{
    ASSERT_EQ(System::String::Format(u"<html>{0}", newLine) + System::String::Format(u"\t<head>{0}", newLine) + System::String::Format(u"\t\t<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />{0}", newLine) + System::String::Format(u"\t\t<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />{0}", newLine) + System::String::Format(u"\t\t<meta name=\"generator\" content=\"{0} {1}\" />{2}", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version(), newLine) + System::String::Format(u"\t\t<title>{0}", newLine) + System::String::Format(u"\t\t</title>{0}", newLine) + System::String::Format(u"\t</head>{0}", newLine) + System::String::Format(u"\t<body style=\"font-family:'Times New Roman'; font-size:12pt\">{0}", newLine) + System::String::Format(u"\t\t<div>{0}", newLine) + System::String::Format(u"\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">{0}", newLine) + System::String::Format(u"\t\t\t\t<span>Hello world!</span>{0}", newLine) + System::String::Format(u"\t\t\t</p>{0}", newLine) + System::String::Format(u"\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">{0}", newLine) + System::String::Format(u"\t\t\t\t<span style=\"-aw-import:ignore\">&#xa0;</span>{0}", newLine) + System::String::Format(u"\t\t\t</p>{0}", newLine) + System::String::Format(u"\t\t</div>{0}", newLine) + System::String::Format(u"\t</body>{0}</html>", newLine), html);
}
else
{
    ASSERT_EQ(System::String(u"<html><head><meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />") + u"<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />" + System::String::Format(u"<meta name=\"generator\" content=\"{0} {1}\" /><title></title></head>", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) + u"<body style=\"font-family:'Times New Roman'; font-size:12pt\">" + u"<div><p style=\"margin-top:0pt; margin-bottom:0pt\"><span>Hello world!</span></p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\"><span style=\"-aw-import:ignore\">&#xa0;</span></p></div></body></html>", html);
}
```

## См. также

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
