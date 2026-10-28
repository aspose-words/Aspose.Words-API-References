---
title: Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes method
linktitle: get_RenderNonImageShapes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes method. Gets or sets a value indicating whether non-image shapes should be rendered and written to the output Docling JSON document in C++.'
type: docs
weight: 6500
url: /cpp/aspose.words.saving/doclingsaveoptions/get_rendernonimageshapes/
---
## DoclingSaveOptions::get_RenderNonImageShapes method


Gets or sets a value indicating whether non-image shapes should be rendered and written to the output Docling JSON document.

```cpp
_Bool Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes() const
```

## Remarks

 If the property is false, non-image shapes are not exported to the output document. The default value is false. 
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
