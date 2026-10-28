---
title: Aspose::Words::Saving::MarkdownSaveOptions::set_ExportUnderlineFormatting method
linktitle: set_ExportUnderlineFormatting
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownSaveOptions::set_ExportUnderlineFormatting method. Sets a boolean value indicating either to export underline text formatting as sequence of two plus characters "++". The default value is false in C++.'
type: docs
weight: 11500
url: /cpp/aspose.words.saving/markdownsaveoptions/set_exportunderlineformatting/
---
## MarkdownSaveOptions::set_ExportUnderlineFormatting method


Sets a boolean value indicating either to export underline text formatting as sequence of two plus characters "++". The default value is **false**.

```cpp
void Aspose::Words::Saving::MarkdownSaveOptions::set_ExportUnderlineFormatting(bool value)
```

## Examples


Shows how to export underline formatting as ++.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Underline::Single);
builder->Write(u"Lorem ipsum. Dolor sit amet.");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportUnderlineFormatting(true);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```
## See Also

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
