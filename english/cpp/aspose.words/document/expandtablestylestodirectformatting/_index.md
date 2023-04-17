---
title: Aspose::Words::Document::ExpandTableStylesToDirectFormatting method
linktitle: ExpandTableStylesToDirectFormatting
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::ExpandTableStylesToDirectFormatting method. Converts formatting specified in table styles into direct formatting on tables in the document in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words/document/expandtablestylestodirectformatting/
---
## Document::ExpandTableStylesToDirectFormatting method


Converts formatting specified in table styles into direct formatting on tables in the document.

```cpp
void Aspose::Words::Document::ExpandTableStylesToDirectFormatting()
```

## Remarks


This method exists because this version of Aspose.Words provides only limited support for table styles (see below). This method might be useful when you load a DOCX or WordprocessingML document that contains tables formatted with table styles and you need to query formatting of tables, cells, paragraphs or text.

This version of Aspose.Words provides limited support for table styles as follows:

* Table styles defined in DOCX or WordprocessingML documents are preserved as table styles when saving the document as DOCX or WordprocessingML.
* Table styles defined in DOCX or WordprocessingML documents are automatically converted to direct formatting on tables when saving the document into any other format, rendering or printing.
* Table styles defined in DOC documents are preserved as table styles when saving the document as DOC only.



## Examples



Shows how to apply the properties of a table's style directly to the table's elements. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Hello world!");
builder->EndTable();

auto tableStyle = System::DynamicCast<TableStyle>(doc->get_Styles()->Add(StyleType::Table, u"MyTableStyle1"));
tableStyle->set_RowStripe(3);
tableStyle->set_CellSpacing(5);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(LineStyle::DotDash);

table->set_Style(tableStyle);

// This method concerns table style properties such as the ones we set above.
doc->ExpandTableStylesToDirectFormatting();

doc->Save(ArtifactsDir + u"Document.TableStyleToDirectFormatting.docx");
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
