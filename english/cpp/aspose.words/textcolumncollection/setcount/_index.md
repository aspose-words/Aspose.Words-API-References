---
title: SetCount
second_title: Aspose.Words for C++ API Reference
description: Arranges text into the specified number of text columns.
type: docs
weight: 118
url: /cpp/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection::SetCount method


Arranges text into the specified number of text columns.

```cpp
void Aspose::Words::TextColumnCollection::SetCount(int32_t newCount)
```


| Parameter | Type | Description |
| --- | --- | --- |
| newCount | int32_t | The number of columns the text is to be arranged into. |
## Remarks


When [EvenlySpaced](../get_evenlyspaced/) is **false** and you increase the number of columns, new [TextColumn](../../textcolumn/) objects are created with zero width and spacing. You need to set width and spacing for the new columns.

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

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
