---
title: "Aspose::Words::ConditionalStyle Klasse"
linktitle: "ConditionalStyle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ConditionalStyle Klasse. Stellt spezielle Formatierung dar, die auf einen Bereich einer Tabelle mit zugewiesenem Tabellenstil angewendet wird. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 16000
url: /de/cpp/aspose.words/conditionalstyle/
---
## ConditionalStyle class


Stellt eine spezielle Formatierung dar, die auf einen Bereich einer Tabelle mit zugewiesenen Tabellenstil angewendet wird. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class ConditionalStyle : public Aspose::Words::IBorderAttrSource,
                         public Aspose::Words::IShadingAttrSource,
                         public Aspose::Words::IParaAttrSource,
                         public Aspose::Words::IRunAttrSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Löscht die Formatierung dieses bedingten Stils. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Vergleicht diesen bedingten Stil mit dem angegebenen Objekt. |
| [get_Borders](./get_borders/)() | Ruft die Sammlung der Standardzellenränder für den bedingten Stil ab. |
| [get_BottomPadding](./get_bottompadding/)() | Ruft den Abstand (in Punkten) ab oder legt ihn fest, der unter dem Inhalt von Tabellenzellen hinzugefügt wird. |
| [get_Font](./get_font/)() | Ruft die Zeichenformatierung des bedingten Stils ab. |
| [get_LeftPadding](./get_leftpadding/)() | Ruft den Abstand (in Punkten) ab oder legt ihn fest, der links vom Inhalt von Tabellenzellen hinzugefügt wird. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Ruft die Absatzformatierung des bedingten Stils ab. |
| [get_RightPadding](./get_rightpadding/)() | Ruft den Abstand (in Punkten) ab oder legt ihn fest, der rechts vom Inhalt von Tabellenzellen hinzugefügt wird. |
| [get_Shading](./get_shading/)() | Ruft ein [Shading](../shading/)‑Objekt ab, das sich auf die Schattierungsformatierung für diesen bedingten Stil bezieht. |
| [get_TopPadding](./get_toppadding/)() | Ruft den Abstand (in Punkten) ab oder legt ihn fest, der über dem Inhalt von Tabellenzellen hinzugefügt wird. |
| [get_Type](./get_type/)() | Ruft den Tabellenbereich ab, auf den sich dieser bedingte Stil bezieht. |
| [GetHashCode](./gethashcode/)() const override | Berechnet den Hashcode für dieses Objekt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | Setter für [Aspose::Words::ConditionalStyle::get_BottomPadding](./get_bottompadding/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Setter für [Aspose::Words::ConditionalStyle::get_LeftPadding](./get_leftpadding/). |
| [set_RightPadding](./set_rightpadding/)(double) | Setter für [Aspose::Words::ConditionalStyle::get_RightPadding](./get_rightpadding/). |
| [set_TopPadding](./set_toppadding/)(double) | Setter für [Aspose::Words::ConditionalStyle::get_TopPadding](./get_toppadding/). |
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
