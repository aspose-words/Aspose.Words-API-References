---
title: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize"
linktitle: "get_ExportRelativeFontSize"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize. Указывает, должны ли размеры шрифтов выводиться в относительных единицах при сохранении в HTML, MHTML или EPUB. По умолчанию — false в C++."
type: docs
weight: 25000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_exportrelativefontsize/
---
## HtmlSaveOptions::get_ExportRelativeFontSize method


Указывает, должны ли размеры шрифтов выводиться в относительных единицах при сохранении в HTML, MHTML или EPUB. По умолчанию **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize() const
```

## Примечания


Во многих существующих документах (HTML, IDPF EPUB) размеры шрифтов указаны в относительных единицах. Это позволяет приложениям регулировать размер текста при просмотре/обработке документов. Например, в Microsoft Internet Explorer есть подменю "View->Text Size", в Adobe Digital Editions есть две кнопки: Increase/Decrease Text Size. Если вы ожидаете, что эта функция будет работать, установите свойство [ExportRelativeFontSize](./) в **true**.

**Aspose**[Words](../../../aspose.words/) document model contains and operates only with absolute font size units. Relative units need additional logic to be recalculated from some initial (standard) size. [Font](../../../aspose.words/font/) size of **Normal** document style is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output as **%1.5em.** to the HTML.

Когда эта опция включена, элементы документа, кроме текста, по‑прежнему будут иметь абсолютные размеры. Также некоторые атрибуты, связанные с текстом, могут быть выражены абсолютно. В частности, межстрочный интервал, указанный правилом "exactly", может давать нежелательные результаты при масштабировании текста. Поэтому исходные документы должны быть правильно спроектированы и протестированы при экспорте с параметром [ExportRelativeFontSize](./), установленным в **true**.

## Примеры



Показывает, как использовать относительные размеры шрифтов при сохранении в .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Default font size, ");
builder->get_Font()->set_Size(24);
builder->Writeln(u"2x default font size,");
builder->get_Font()->set_Size(96);
builder->Write(u"8x default font size");

// При сохранении документа в HTML мы можем передать объект SaveOptions
// для определения, использовать относительные или абсолютные размеры шрифтов.
// Установите флаг "ExportRelativeFontSize" в "true", чтобы объявить размеры шрифтов
// используя единицу измерения "em", которая является коэффициентом, умножающим текущий размер шрифта.
// Установите флаг "ExportRelativeFontSize" в "false", чтобы объявить размеры шрифтов
// используя единицу измерения "pt", которая представляет собой абсолютный размер шрифта в пунктах.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportRelativeFontSize(exportRelativeFontSize);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'; font-size:12pt\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
