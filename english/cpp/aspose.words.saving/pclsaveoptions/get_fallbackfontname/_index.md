---
title: get_FallbackFontName
second_title: Aspose.Words for C++ API Reference
description: Name of the font that will be used if no expected font is found in printer and built-in fonts collections.
type: docs
weight: 27
url: /cpp/aspose.words.saving/pclsaveoptions/get_fallbackfontname/
---
## PclSaveOptions::get_FallbackFontName method


Name of the font that will be used if no expected font is found in printer and built-in fonts collections.

```cpp
System::String Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName() const
```


## Examples



Shows how to declare a font that a printer will apply to printed text as a substitute should its original font be unavailable. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

auto saveOptions = MakeObject<PclSaveOptions>();
saveOptions->set_FallbackFontName(u"Times New Roman");

// This document will instruct the printer to apply "Times New Roman" to the text with the missing font.
// Should "Times New Roman" also be unavailable, the printer will default to the "Arial" font.
doc->Save(ArtifactsDir + u"PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

## See Also

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
