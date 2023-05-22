---
title: Aspose::Words::Tables::CellFormat::SetPaddings method
linktitle: SetPaddings
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::CellFormat::SetPaddings method. Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell in C++.'
type: docs
weight: 31000
url: /cpp/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat::SetPaddings method


Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell.

```cpp
void Aspose::Words::Tables::CellFormat::SetPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


## Examples



Shows how to pad the contents of a cell with whitespace. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Set a padding distance (in points) between the border and the text contents
// of each table cell we create with the document builder.
builder->get_CellFormat()->SetPaddings(5, 10, 40, 50);

// Create a table with one cell whose contents will have whitespace padding.
builder->StartTable();
builder->InsertCell();
builder->Write(String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") +
               u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(ArtifactsDir + u"CellFormat.Padding.docx");
```

## See Also

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
