---
title: "Aspose::Words::TableStyle::get_VerticalAlignment Methode"
linktitle: "get_VerticalAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TableStyle::get_VerticalAlignment Methode. Gibt die vertikale Ausrichtung für die Zellen in C++ an."
type: docs
weight: 16000
url: /de/cpp/aspose.words/tablestyle/get_verticalalignment/
---
## TableStyle::get_VerticalAlignment method


Gibt die vertikale Ausrichtung für die Zellen an.

```cpp
Aspose::Words::Tables::CellVerticalAlignment Aspose::Words::TableStyle::get_VerticalAlignment()
```


## Beispiele



Zeigt, wie benutzerdefinierte Stileinstellungen für die Tabelle erstellt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Name");
builder->InsertCell();
builder->Write(u"مرحبًا");
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_AllowBreakAcrossPages(true);
tableStyle->set_CellSpacing(5);
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(5);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
tableStyle->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);

table->set_Style(tableStyle);

// Das Festlegen der Stil‑Eigenschaften einer Tabelle kann die Eigenschaften der Tabelle selbst beeinflussen.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## Siehe auch

* Enum [CellVerticalAlignment](../../../aspose.words.tables/cellverticalalignment/)
* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
