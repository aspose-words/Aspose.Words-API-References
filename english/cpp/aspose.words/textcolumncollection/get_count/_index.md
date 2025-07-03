---
title: Aspose::Words::TextColumnCollection::get_Count method
linktitle: get_Count
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TextColumnCollection::get_Count method. Gets the number of columns in the section of a document in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/textcolumncollection/get_count/
---
## TextColumnCollection::get_Count method


Gets the number of columns in the section of a document.

```cpp
int32_t Aspose::Words::TextColumnCollection::get_Count()
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
