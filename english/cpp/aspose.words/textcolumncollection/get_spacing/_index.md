---
title: Aspose::Words::TextColumnCollection::get_Spacing method
linktitle: get_Spacing
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TextColumnCollection::get_Spacing method. When columns are evenly spaced, gets or sets the amount of space between each column in points in C++.'
type: docs
weight: 5000
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
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## See Also

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
