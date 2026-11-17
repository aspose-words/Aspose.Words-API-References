---
title: Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting method
linktitle: get_ContextTableFormatting
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting method. True if the formatting applied to table content does not affect the formatting of the content that follows it. Default value is true in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/documentbuilderoptions/get_contexttableformatting/
---
## DocumentBuilderOptions::get_ContextTableFormatting method


True if the formatting applied to table content does not affect the formatting of the content that follows it. Default value is **true**.

```cpp
bool Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting() const
```


## Examples



Shows how to ignore table formatting for content after. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// Adds content before the table.
// Default font size is 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// Changes the font size inside the table.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// If ContextTableFormatting is true, then table formatting isn't applied to the content after.
// If ContextTableFormatting is false, then table formatting is applied to the content after.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## See Also

* Class [DocumentBuilderOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
