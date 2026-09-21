---
title: "Aspose::Words::ConditionalStyle class"
linktitle: "ConditionalStyle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ConditionalStyle class. Representerar speciell formatering som tillämpas på ett område i en tabell med tilldelad tabellstil. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words/conditionalstyle/
---
## ConditionalStyle class


Representerar speciell formatering som tillämpas på ett område i en tabell med tilldelad tabellstil. För att läsa mer, besök dokumentationsartikeln [Arbeta med tabeller](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class ConditionalStyle : public Aspose::Words::IBorderAttrSource,
                         public Aspose::Words::IShadingAttrSource,
                         public Aspose::Words::IParaAttrSource,
                         public Aspose::Words::IRunAttrSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Rensar formatering av denna villkorliga stil. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Jämför denna villkorliga stil med det angivna objektet. |
| [get_Borders](./get_borders/)() | Hämtar samlingen av standardcellramar för den villkorliga stilen. |
| [get_BottomPadding](./get_bottompadding/)() | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till under innehållet i tabellceller. |
| [get_Font](./get_font/)() | Hämtar teckenformateringen för den villkorliga stilen. |
| [get_LeftPadding](./get_leftpadding/)() | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till till vänster om innehållet i tabellceller. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Hämtar styckeformateringen för den villkorliga stilen. |
| [get_RightPadding](./get_rightpadding/)() | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till till höger om innehållet i tabellceller. |
| [get_Shading](./get_shading/)() | Hämtar ett [Shading](../shading/)‑objekt som hänvisar till skuggningsformateringen för denna villkorliga stil. |
| [get_TopPadding](./get_toppadding/)() | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till ovanför innehållet i tabellceller. |
| [get_Type](./get_type/)() | Hämtar tabellområde som denna villkorliga stil relaterar till. |
| [GetHashCode](./gethashcode/)() const override | Beräknar hashkod för detta objekt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | Sättare för [Aspose::Words::ConditionalStyle::get_BottomPadding](./get_bottompadding/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Sättare för [Aspose::Words::ConditionalStyle::get_LeftPadding](./get_leftpadding/). |
| [set_RightPadding](./set_rightpadding/)(double) | Sättare för [Aspose::Words::ConditionalStyle::get_RightPadding](./get_rightpadding/). |
| [set_TopPadding](./set_toppadding/)(double) | Sättare för [Aspose::Words::ConditionalStyle::get_TopPadding](./get_toppadding/). |
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
