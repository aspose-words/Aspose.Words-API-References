---
title: Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting method
linktitle: get_ExportUnderlineFormatting
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting method. Gets or sets a boolean value indicating either to export underline text formatting as sequence of two plus characters "++". The default value is false in C++.'
type: docs
weight: 3500
url: /cpp/aspose.words.saving/markdownsaveoptions/get_exportunderlineformatting/
---
## MarkdownSaveOptions::get_ExportUnderlineFormatting method


Gets or sets a boolean value indicating either to export underline text formatting as sequence of two plus characters "++". The default value is **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting() const
```


## Examples



Shows how to export underline formatting as ++. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Single);
builder->Write(u"Lorem ipsum. Dolor sit amet.");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportUnderlineFormatting(true);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

## See Also

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
