---
title: Aspose::Words::Tables::Cell::get_FirstParagraph method
linktitle: get_FirstParagraph
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Cell::get_FirstParagraph method. Gets the first paragraph among the immediate children in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.tables/cell/get_firstparagraph/
---
## Cell::get_FirstParagraph method


Gets the first paragraph among the immediate children.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Tables::Cell::get_FirstParagraph()
```


## Examples



Shows how to create a nested table using a document builder. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Build the outer table.
System::SharedPtr<Aspose::Words::Tables::Cell> cell = builder->InsertCell();
builder->Writeln(u"Outer Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Outer Table Cell 2");
builder->EndTable();

// Move to the first cell of the outer table, the build another table inside the cell.
builder->MoveTo(cell->get_FirstParagraph());
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 2");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertNestedTable.docx");
```

## See Also

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
