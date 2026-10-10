---
title: "Aspose::Words::TableStyle::get_LeftIndent metod"
linktitle: "get_LeftIndent"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TableStyle::get_LeftIndent metod. Hämtar eller anger värdet som representerar vänsterindraget för en tabell i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words/tablestyle/get_leftindent/
---
## TableStyle::get_LeftIndent method


Hämtar eller anger värdet som representerar vänsterindraget för en tabell.

```cpp
double Aspose::Words::TableStyle::get_LeftIndent()
```


## Exempel



Visar hur man ställer in positionen för en tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan finns två sätt att justera en tabell horisontellt.
// 1 -  Använd egenskapen "Alignment" för att justera den till en plats på sidan, till exempel mitten:
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

// Infoga en tabell och tillämpa den stil vi skapade på den.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned to the center of the page");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

// 2 -  Använd "LeftIndent" för att ange ett indrag från sidans vänstra marginal:
tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle2"));
tableStyle->set_LeftIndent(55);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Green());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned according to left indent");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

doc->Save(get_ArtifactsDir() + u"Table.SetTableAlignment.docx");
```

## Se även

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
