---
title: "Aspose::Words::TableStyle::get_LeftIndent Methode"
linktitle: "get_LeftIndent"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TableStyle::get_LeftIndent Methode. Liest oder setzt den Wert, der den linken Einzug einer Tabelle in C++ darstellt."
type: docs
weight: 10000
url: /de/cpp/aspose.words/tablestyle/get_leftindent/
---
## TableStyle::get_LeftIndent method


Ruft ab oder legt den Wert fest, der den linken Einzug einer Tabelle darstellt.

```cpp
double Aspose::Words::TableStyle::get_LeftIndent()
```


## Beispiele



Zeigt, wie die Position einer Tabelle festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind zwei Möglichkeiten, eine Tabelle horizontal auszurichten.
// 1 -  Verwenden Sie die Eigenschaft "Alignment", um sie an einer Position auf der Seite auszurichten, z. B. in der Mitte:
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

// Fügen Sie eine Tabelle ein und wenden Sie den von uns erstellten Stil darauf an.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned to the center of the page");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

// 2 -  Verwenden Sie "LeftIndent", um einen Einzug vom linken Seitenrand anzugeben:
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

## Siehe auch

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
