---
title: "Aspose::Words::TableStyle::get_ColumnStripe metod"
linktitle: "get_ColumnStripe"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TableStyle::get_ColumnStripe metod. Hämtar eller anger ett antal kolumner som ska inkluderas i bandningen när stilen specificerar udda/jämna kolumnband i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/tablestyle/get_columnstripe/
---
## TableStyle::get_ColumnStripe method


Hämtar eller anger antalet kolumner som ska inkluderas i bandning när stilen specificerar ojämna/jämna kolumnband.

```cpp
int32_t Aspose::Words::TableStyle::get_ColumnStripe()
```


## Exempel



Visar hur man skapar villkorliga tabellstilar som växlar mellan rader.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Vi kan konfigurera en villkorlig stil för en tabell för att tillämpa en annan färg på raden/kolumnen,
// baserat på om raden/kolumnen är jämn eller ojämn, vilket skapar ett växlande färgmönster.
// Vi kan också tillämpa ett tal n på rad-/kolumnbandningen,
// vilket betyder att färgen växlar efter varje n rad/kolumn istället för en.
// Skapa en tabell där enskilda kolumner och rader bandas, kolumnerna bandas i grupper om tre.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
for (int32_t i = 0; i < 15; i++)
{
    for (int32_t j = 0; j < 4; j++)
    {
        builder->InsertCell();
        builder->Writeln(System::String::Format(u"{0} column.", (j % 2 == 0 ? System::String(u"Even") : System::String(u"Odd"))));
        builder->Write(System::String::Format(u"Row banding {0}.", (i % 3 == 0 ? System::String(u"start") : System::String(u"continuation"))));
    }
    builder->EndRow();
}
builder->EndTable();

// Applicera en linjestil på alla tabellens kanter.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);

// Ställ in de två färgerna, som kommer att växla var tredje rad.
tableStyle->set_RowStripe(3);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::OddRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightCyan());

// Ställ in en färg som ska tillämpas på varje jämn kolumn, vilket kommer att åsidosätta eventuell anpassad radfärgning.
tableStyle->set_ColumnStripe(1);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenColumnBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSalmon());

table->set_Style(tableStyle);

// Egenskapen "StyleOptions" aktiverar radbandning som standard.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// Använd också egenskapen "StyleOptions" för att aktivera kolumnbandning.
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::ColumnBands);

doc->Save(get_ArtifactsDir() + u"Table.AlternatingRowStyles.docx");
```

## Se även

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
