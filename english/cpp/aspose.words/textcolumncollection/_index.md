---
title: Aspose::Words::TextColumnCollection class
linktitle: TextColumnCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TextColumnCollection class. A collection of TextColumn objects that represent all the columns of text in a section of a document. To learn more, visit the  documentation article in C++.'
type: docs
weight: 71000
url: /cpp/aspose.words/textcolumncollection/
---
## TextColumnCollection class


A collection of [TextColumn](../textcolumn/) objects that represent all the columns of text in a section of a document. To learn more, visit the [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/) documentation article.

```cpp
class TextColumnCollection : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Count](./get_count/)() | Gets the number of columns in the section of a document. |
| [get_EvenlySpaced](./get_evenlyspaced/)() | True if text columns are of equal width and evenly spaced. |
| [get_LineBetween](./get_linebetween/)() | When **true**, adds a vertical line between columns. |
| [get_Spacing](./get_spacing/)() | When columns are evenly spaced, gets or sets the amount of space between each column in points. |
| [get_Width](./get_width/)() | When columns are evenly spaced, gets the width of the columns. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returns a text column at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EvenlySpaced](./set_evenlyspaced/)(bool) | Setter for [Aspose::Words::TextColumnCollection::get_EvenlySpaced](./get_evenlyspaced/). |
| [set_LineBetween](./set_linebetween/)(bool) | Setter for [Aspose::Words::TextColumnCollection::get_LineBetween](./get_linebetween/). |
| [set_Spacing](./set_spacing/)(double) | Setter for [Aspose::Words::TextColumnCollection::get_Spacing](./get_spacing/). |
| [SetCount](./setcount/)(int32_t) | Arranges text into the specified number of text columns. |
| static [Type](./type/)() |  |
## Remarks


Use [SetCount()](./setcount/) to set the number of text columns.

To make all columns equal width and spaced evenly, set [EvenlySpaced](./get_evenlyspaced/) to **true** and specify the amount of space between the columns in [Spacing](./get_spacing/). MS Word will automatically calculate column widths.

If you have [EvenlySpaced](./get_evenlyspaced/) set to **false**, you need to specify width and spacing for each column individually. Use the indexer to access individual [TextColumn](../textcolumn/) objects.

When using custom column widths, make sure the sum of all column widths and spacings between them equals page width minus left and right page margins.

## Examples



Shows how to create multiple evenly spaced columns in a section. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(ArtifactsDir + u"PageSetup.ColumnsSameWidth.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
