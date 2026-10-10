---
title: "Aspose::Words::ConditionalStyleCollection::ClearFormatting Methode"
linktitle: "ClearFormatting"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ConditionalStyleCollection::ClearFormatting-Methode. Löscht alle bedingten Stile des Tabellenstils in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection::ClearFormatting method


Löscht alle bedingten Stile des Tabellenstils.

```cpp
void Aspose::Words::ConditionalStyleCollection::ClearFormatting()
```


## Beispiele



Zeigt, wie man bedingte Tabellenstile zurücksetzt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"First row");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Last row");
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
table->set_Style(tableStyle);

// Setzt den Tabellenstil, um die Ränder der ersten Zeile der Tabelle rot zu färben.
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->set_Color(System::Drawing::Color::get_Red());

// Setzt den Tabellenstil, um die Ränder der letzten Zeile der Tabelle blau zu färben.
tableStyle->get_ConditionalStyles()->get_LastRow()->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// Unten sind zwei Möglichkeiten, die "ClearFormatting"-Methode zu verwenden, um die bedingten Stile zu löschen.
// 1 -  Lösche die bedingten Stile für einen bestimmten Teil einer Tabelle:
tableStyle->get_ConditionalStyles()->idx_get(0)->ClearFormatting();

ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->get_Color());

// 2 -  Lösche die bedingten Stile für die gesamte Tabelle:
tableStyle->get_ConditionalStyles()->ClearFormatting();

ASSERT_TRUE(tableStyle->get_ConditionalStyles()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::ConditionalStyle>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::ConditionalStyle> s)>>([](System::SharedPtr<Aspose::Words::ConditionalStyle> s) -> bool
{
    return s->get_Borders()->get_Color() == System::Drawing::Color::Empty;
}))));
```

## Siehe auch

* Class [ConditionalStyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
