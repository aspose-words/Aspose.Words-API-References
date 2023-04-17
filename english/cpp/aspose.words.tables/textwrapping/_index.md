---
title: Aspose::Words::Tables::TextWrapping enum
linktitle: TextWrapping
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::TextWrapping enum. Specifies how text is wrapped around the table in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.tables/textwrapping/
---
## TextWrapping enum


Specifies how text is wrapped around the table.

```cpp
enum class TextWrapping
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | Text and table is displayed in the order of their appearance in the document. |
| Around | 1 | Text is wrapped around the table occupying available side space. |
| Default | n/a | Default value. |


## Examples



Shows how to work with table text wrapping. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndTable();
table->set_PreferredWidth(PreferredWidth::FromPoints(300));

builder->get_Font()->set_Size(16);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Set the "TextWrapping" property to "TextWrapping.Around" to get the table to wrap text around it,
// and push it down into the paragraph below by setting the position.
table->set_TextWrapping(TextWrapping::Around);
table->set_AbsoluteHorizontalDistance(100);
table->set_AbsoluteVerticalDistance(20);

doc->Save(ArtifactsDir + u"Table.WrapText.docx");
```

## See Also

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
