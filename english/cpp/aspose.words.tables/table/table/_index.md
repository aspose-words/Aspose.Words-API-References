---
title: Aspose::Words::Tables::Table::Table constructor
linktitle: Table
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::Table constructor. Initializes a new instance of the Table class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.tables/table/table/
---
## Table::Table constructor


Initializes a new instance of the [Table](../) class.

```cpp
Aspose::Words::Tables::Table::Table(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
## Remarks


When [Table](../) is created, it belongs to the specified document, but is not yet part of the document and [ParentNode](../../../aspose.words/node/get_parentnode/) is **null**.

To append [Table](../) to the document use [InsertAfter1()</see> or <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) on the story where you want the table inserted.

## Examples



Shows how to create a table. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Tables contain rows, which contain cells, which may have paragraphs
// with typical elements such as runs, shapes, and even other tables.
// Calling the "EnsureMinimum" method on a table will ensure that
// the table has at least one row, cell, and paragraph.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// Add text to the first cell in the first row of the table.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```

## See Also

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
