---
title: Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix method
linktitle: get_IdPrefix
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix method. Specifies a prefix that is prepended to all generated element IDs in the output document. Default value is null and no prefix is prepended in C++.'
type: docs
weight: 4250
url: /cpp/aspose.words.saving/svgsaveoptions/get_idprefix/
---
## SvgSaveOptions::get_IdPrefix method


Specifies a prefix that is prepended to all generated element IDs in the output document. Default value is null and no prefix is prepended.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix() const
```


## Examples



Shows how to add a prefix that is prepended to all generated element IDs (svg). 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

## See Also

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
