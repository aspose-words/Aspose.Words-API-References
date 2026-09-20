---
title: "Aspose::Words::Saving::HtmlElementSizeOutputMode enum"
linktitle: "HtmlElementSizeOutputMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlElementSizeOutputMode enum. Указывает, как Aspose.Words экспортирует ширину и высоту элементов в HTML, MHTML и EPUB в C++."
type: docs
weight: 58000
url: /ru/cpp/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enum


Указывает, как Aspose.Words экспортирует ширину и высоту элементов в HTML, MHTML и EPUB.

```cpp
enum class HtmlElementSizeOutputMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Все | 0 | Все размеры элементов, как в абсолютных, так и в относительных единицах, указанные в документе, экспортируются. |
| RelativeOnly | 1 | Размеры элементов экспортируются только в том случае, если они указаны в относительных единицах в документе. Фиксированные размеры не экспортируются в этом режиме. Визуальные агенты вычислят недостающие размеры, чтобы сделать макет документа более естественным. |
| None | 2 | Размеры элементов не экспортируются. Визуальные агенты автоматически построят макет в соответствии с взаимосвязью между элементами. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
