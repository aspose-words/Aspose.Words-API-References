---
title: "Aspose::Words::TableStyle::get_Shading Methode"
linktitle: "get_Shading"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TableStyle::get_Shading Methode. Gibt ein Shading-Objekt zurück, das sich auf die Schattierungsformatierung für Tabellenzellen in C++ bezieht."
type: docs
weight: 14000
url: /de/cpp/aspose.words/tablestyle/get_shading/
---
## TableStyle::get_Shading method


Gibt ein [Shading](../../shading/) Objekt zurück, das sich auf die Schattierungsformatierung für Tabellenzellen bezieht.

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::TableStyle::get_Shading()
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

* Class [Shading](../../shading/)
* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
