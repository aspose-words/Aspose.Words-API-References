---
title: "Aspose::Words::ConditionalStyleCollection Klasse"
linktitle: "ConditionalStyleCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ConditionalStyleCollection Klasse. Stellt eine Sammlung von ConditionalStyle‑Objekten dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 17000
url: /de/cpp/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class


Stellt eine Sammlung von [ConditionalStyle](../conditionalstyle/)‑Objekten dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class ConditionalStyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::ConditionalStyle>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Löscht alle bedingten Stile des Tabellenstils. |
| [get_BottomLeftCell](./get_bottomleftcell/)() | Ruft den Stil der unteren linken Zelle ab. |
| [get_BottomRightCell](./get_bottomrightcell/)() | Ruft den Stil der Zelle unten rechts ab. |
| [get_Count](./get_count/)() const | Ruft die Anzahl der bedingten Stile in der Sammlung ab. |
| [get_EvenColumnBanding](./get_evencolumnbanding/)() | Ruft den Stil für gerade Spaltenbänder ab. |
| [get_EvenRowBanding](./get_evenrowbanding/)() | Ruft den Stil für gerade Zeilenbänder ab. |
| [get_FirstColumn](./get_firstcolumn/)() | Ruft den Stil der ersten Spalte ab. |
| [get_FirstRow](./get_firstrow/)() | Ruft den Stil der ersten Zeile ab. |
| [get_LastColumn](./get_lastcolumn/)() | Ruft den Stil der letzten Spalte ab. |
| [get_LastRow](./get_lastrow/)() | Ruft den Stil der letzten Zeile ab. |
| [get_OddColumnBanding](./get_oddcolumnbanding/)() | Ruft den Stil für ungerade Spaltenbänder ab. |
| [get_OddRowBanding](./get_oddrowbanding/)() | Ruft den Stil für ungerade Zeilenbänder ab. |
| [get_TopLeftCell](./get_topleftcell/)() | Ruft den Stil der Zelle oben links ab. |
| [get_TopRightCell](./get_toprightcell/)() | Ruft den Stil der Zelle oben rechts ab. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator-Objekt zurück, das verwendet werden kann, um über alle bedingten Stile in der Sammlung zu iterieren. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::ConditionalStyleType) | Ruft ein [ConditionalStyle](../conditionalstyle/)-Objekt anhand des bedingten Stiltyps ab. |
| [idx_get](./idx_get/)(int32_t) | Ruft ein [ConditionalStyle](../conditionalstyle/)-Objekt anhand des Index ab. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man mit bestimmten Bereichsstilen einer Tabelle arbeitet.
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

// Erstelle einen benutzerdefinierten Tabellenstil.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));

// Bedingte Stile sind Formatierungsänderungen, die nur einige Zellen der Tabelle betreffen
// basierend auf einer Bedingung, wie zum Beispiel dass die Zellen in der letzten Zeile liegen.
// Unten sind drei Möglichkeiten aufgeführt, um auf die bedingten Stile eines Tabellenstils aus der "ConditionalStyles"-Sammlung zuzugreifen.
// 1 -  Nach Stiltyp:
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::FirstRow)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AliceBlue());

// 2 -  Nach Index:
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
ASSERT_EQ(Aspose::Words::ConditionalStyleType::FirstRow, tableStyle->get_ConditionalStyles()->idx_get(0)->get_Type());

// 3 -  Als Eigenschaft:
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

// Wende Abstand und Textformatierung auf bedingte Stile an.
tableStyle->get_ConditionalStyles()->get_LastRow()->set_BottomPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_LeftPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_RightPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_TopPadding(10);
tableStyle->get_ConditionalStyles()->get_LastColumn()->get_Font()->set_Bold(true);

// Liste alle möglichen Stilbedingungen auf.
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

// Wende den benutzerdefinierten Stil, der alle bedingten Stile enthält, auf die Tabelle an.
table->set_Style(tableStyle);

// Unser Stil wendet standardmäßig einige bedingte Stile an.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// Wir müssen alle anderen Stile selbst über die Eigenschaft "StyleOptions" aktivieren.
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::LastRow | Aspose::Words::Tables::TableStyleOptions::LastColumn);

doc->Save(get_ArtifactsDir() + u"Table.ConditionalStyles.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
