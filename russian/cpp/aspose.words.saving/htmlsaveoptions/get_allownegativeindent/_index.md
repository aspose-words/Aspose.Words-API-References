---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent метод"
linktitle: "get_AllowNegativeIndent"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent метод. Указывает, нормализуются ли отрицательные левый и правый отступы абзацев при сохранении в HTML, MHTML или EPUB. Значение по умолчанию — false в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_allownegativeindent/
---
## HtmlSaveOptions::get_AllowNegativeIndent method


Указывает, нормализуются ли отрицательные левый и правый отступы абзацев при сохранении в форматы HTML, MHTML или EPUB. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent() const
```

## Примечания


Когда отрицательный отступ не разрешён, он экспортируется как нулевой отступ в HTML. Когда отрицательный отступ разрешён, абзац может частично выходить за пределы окна браузера.

## Примеры



Показывает, как сохранить отрицательные отступы в выходном .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте таблицу с отрицательным отступом, который сдвинет её влево за левую границу страницы.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(-36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

// Вставьте таблицу с положительным отступом, который сдвинет таблицу вправо.
table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

// При сохранении документа в HTML Aspose.Words будет сохранять только отрицательные отступы
// например, тот, который мы применили к первой таблице, если установим флаг "AllowNegativeIndent"
// в объекте SaveOptions, который мы передадим со значением "true".
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_AllowNegativeIndent(allowNegativeIndent);
options->set_TableWidthOutputMode(Aspose::Words::Saving::HtmlElementSizeOutputMode::RelativeOnly);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
