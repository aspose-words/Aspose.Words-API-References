---
title: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode"
linktitle: "get_TableWidthOutputMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode. Управляет тем, как экспортируются ширины таблиц, строк и ячеек в HTML, MHTML или EPUB. Значение по умолчанию — All в C++."
type: docs
weight: 47000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_tablewidthoutputmode/
---
## HtmlSaveOptions::get_TableWidthOutputMode method


Управляет тем, как экспортируются ширины таблиц, строк и ячеек в HTML, MHTML или EPUB. Значение по умолчанию — [All](../../htmlelementsizeoutputmode/).

```cpp
Aspose::Words::Saving::HtmlElementSizeOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode() const
```

## Примечания


В формате HTML элементы таблицы, строки и ячейки (**%<table>**, **%<tr>**, **%<th>**, **%<td>**) могут иметь указанные ширины либо в относительных (процентных), либо в абсолютных единицах. В документе Aspose.Words таблицы, строки и ячейки также могут иметь ширины, задаваемые как относительными, так и абсолютными единицами.

При конвертации документа в HTML с помощью Aspose.Words вы можете захотеть контролировать, как экспортируются ширины таблиц, строк и ячеек, чтобы влиять на отображение полученного документа в визуальном агенте (например, в браузере или просмотрщике).

Используйте это свойство как фильтр, чтобы указать, какие значения ширины таблиц экспортируются в целевой документ. Например, если вы конвертируете документ в EPUB и планируете просматривать его на мобильном устройстве для чтения, вероятно, вы захотите избежать экспорта абсолютных значений ширины. Для этого необходимо задать режим вывода [RelativeOnly](../../htmlelementsizeoutputmode/) или [None](../../htmlelementsizeoutputmode/), чтобы просмотрщик на мобильном устройстве мог разместить таблицу, максимально заполняя ширину экрана.

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

* Enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
