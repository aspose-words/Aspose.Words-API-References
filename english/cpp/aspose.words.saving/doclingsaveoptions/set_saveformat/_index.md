---
title: Aspose::Words::Saving::DoclingSaveOptions::set_SaveFormat method
linktitle: set_SaveFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::DoclingSaveOptions::set_SaveFormat method. Specifies the format in which the document will be saved if this save options object is used. Can only be Docling in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.saving/doclingsaveoptions/set_saveformat/
---
## DoclingSaveOptions::set_SaveFormat method


Specifies the format in which the document will be saved if this save options object is used. Can only be [Docling](../../../aspose.words/saveformat/).

```cpp
void Aspose::Words::Saving::DoclingSaveOptions::set_SaveFormat(Aspose::Words::SaveFormat value) override
```

## Examples


Shows how to save a document into a Docling JSON format.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rendering.docx"));

auto saveOptions = System::MakeObject<Aspose::Words::Saving::DoclingSaveOptions>();
saveOptions->set_SaveFormat(SaveFormat::Docling);
// Set to true to render non-image shapes and include them in the output.
// Set to false (default) to exclude non-image shapes from the output.
saveOptions->set_RenderNonImageShapes(true);

doc->Save(get_ArtifactsDir() + u"Document.DoclingJson.json", saveOptions);
```
## See Also

* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
