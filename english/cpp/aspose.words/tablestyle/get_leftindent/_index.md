---
title: Aspose::Words::TableStyle::get_LeftIndent method
linktitle: get_LeftIndent
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TableStyle::get_LeftIndent method. Gets or sets the value that represents the left indent of a table in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words/tablestyle/get_leftindent/
---
## TableStyle::get_LeftIndent method


Gets or sets the value that represents the left indent of a table.

```cpp
double Aspose::Words::TableStyle::get_LeftIndent()
```


## Examples



Shows how to set the position of a table. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are two ways of aligning a table horizontally.
// 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
auto tableStyle = System::ExplicitCast<TableStyle>(doc->get_Styles()->Add(StyleType::Table, u"MyTableStyle1"));
tableStyle->set_Alignment(TableAlignment::Center);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(LineStyle::Single);

// Insert a table and apply the style we created to it.
SharedPtr<Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned to the center of the page");
builder->EndTable();
table->set_PreferredWidth(PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

// 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
tableStyle = System::ExplicitCast<TableStyle>(doc->get_Styles()->Add(StyleType::Table, u"MyTableStyle2"));
tableStyle->set_LeftIndent(55);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Green());
tableStyle->get_Borders()->set_LineStyle(LineStyle::Single);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned according to left indent");
builder->EndTable();
table->set_PreferredWidth(PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

doc->Save(ArtifactsDir + u"Table.SetTableAlignment.docx");
```

## See Also

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
