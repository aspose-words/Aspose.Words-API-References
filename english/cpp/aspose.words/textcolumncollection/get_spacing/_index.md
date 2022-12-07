---
title: get_Spacing
second_title: Aspose.Words for C++ API Reference
description: When columns are evenly spaced, gets or sets the amount of space between each column in points.
type: docs
weight: 53
url: /cpp/aspose.words/textcolumncollection/get_spacing/
---
## TextColumnCollection::get_Spacing method


When columns are evenly spaced, gets or sets the amount of space between each column in points.

```cpp
double Aspose::Words::TextColumnCollection::get_Spacing()
```


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
