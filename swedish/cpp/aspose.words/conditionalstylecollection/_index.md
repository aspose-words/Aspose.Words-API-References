---
title: "Aspose::Words::ConditionalStyleCollection class"
linktitle: "ConditionalStyleCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ConditionalStyleCollection class. Representerar en samling av ConditionalStyle‑objekt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 17000
url: /sv/cpp/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class


Representerar en samling av [ConditionalStyle](../conditionalstyle/)‑objekt. För att lära dig mer, besök dokumentationsartikeln [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class ConditionalStyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::ConditionalStyle>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Rensar alla villkorliga stilar i tabellstilen. |
| [get_BottomLeftCell](./get_bottomleftcell/)() | Hämtar stil för den nedre vänstra cellen. |
| [get_BottomRightCell](./get_bottomrightcell/)() | Hämtar den nedre högra cellstilen. |
| [get_Count](./get_count/)() const | Hämtar antalet villkorliga stilar i samlingen. |
| [get_EvenColumnBanding](./get_evencolumnbanding/)() | Hämtar stilen för jämna kolumnband. |
| [get_EvenRowBanding](./get_evenrowbanding/)() | Hämtar stilen för jämna radband. |
| [get_FirstColumn](./get_firstcolumn/)() | Hämtar den första kolumnstilen. |
| [get_FirstRow](./get_firstrow/)() | Hämtar den första radstilen. |
| [get_LastColumn](./get_lastcolumn/)() | Hämtar den sista kolumnstilen. |
| [get_LastRow](./get_lastrow/)() | Hämtar den sista radstilen. |
| [get_OddColumnBanding](./get_oddcolumnbanding/)() | Hämtar stilen för udda kolumnband. |
| [get_OddRowBanding](./get_oddrowbanding/)() | Hämtar stilen för udda radband. |
| [get_TopLeftCell](./get_topleftcell/)() | Hämtar den övre vänstra cellstilen. |
| [get_TopRightCell](./get_toprightcell/)() | Hämtar den övre högra cellstilen. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumeratorobjekt som kan användas för att iterera över alla villkorliga stilar i samlingen. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::ConditionalStyleType) | Hämtar ett [ConditionalStyle](../conditionalstyle/) objekt efter villkorlig stiltyp. |
| [idx_get](./idx_get/)(int32_t) | Hämtar ett [ConditionalStyle](../conditionalstyle/) objekt efter index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exempel



Visar hur man arbetar med vissa områdesstilar i en tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Cell 3");
builder->InsertCell();
builder->Write(u"Cell 4");
builder->EndTable();

// Skapa en anpassad tabellstil.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));

// Villkorliga stilar är formateringsändringar som endast påverkar vissa av tabellens celler
// baserat på ett villkor, såsom att cellerna är i den sista raden.
// Nedan följer tre sätt att komma åt en tabellstils villkorliga stilar från "ConditionalStyles"-samlingen.
// 1 -  Efter stiltyp:
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::FirstRow)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AliceBlue());

// 2 -  Efter index:
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
ASSERT_EQ(Aspose::Words::ConditionalStyleType::FirstRow, tableStyle->get_ConditionalStyles()->idx_get(0)->get_Type());

// 3 -  Som en egenskap:
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

// Applicera utfyllnad och textformatering på villkorliga stilar.
tableStyle->get_ConditionalStyles()->get_LastRow()->set_BottomPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_LeftPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_RightPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_TopPadding(10);
tableStyle->get_ConditionalStyles()->get_LastColumn()->get_Font()->set_Bold(true);

// Lista alla möjliga stilvillkor.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::ConditionalStyle>>> enumerator = tableStyle->get_ConditionalStyles()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::ConditionalStyle> currentStyle = enumerator->get_Current();
        if (currentStyle != nullptr)
        {
            std::cout << System::EnumGetName(currentStyle->get_Type()) << std::endl;
        }
    }
}

// Applicera den anpassade stilen, som innehåller alla villkorliga stilar, på tabellen.
table->set_Style(tableStyle);

// Vår stil tillämpar vissa villkorliga stilar som standard.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// Vi kommer behöva aktivera alla andra stilar själva via egenskapen "StyleOptions".
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::LastRow | Aspose::Words::Tables::TableStyleOptions::LastColumn);

doc->Save(get_ArtifactsDir() + u"Table.ConditionalStyles.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
