---
title: Aspose::Words::Saving::SvgSaveOptions::set_IdPrefix method
linktitle: set_IdPrefix
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SvgSaveOptions::set_IdPrefix method. Specifies a prefix that is prepended to all generated element IDs in the output document. Default value is null and no prefix is prepended in C++.'
type: docs
weight: 14250
url: /cpp/aspose.words.saving/svgsaveoptions/set_idprefix/
---
## SvgSaveOptions::set_IdPrefix method


Specifies a prefix that is prepended to all generated element IDs in the output document. Default value is null and no prefix is prepended.

```cpp
void Aspose::Words::Saving::SvgSaveOptions::set_IdPrefix(const System::String & value)
```

## Remarks

 If the prefix is specified, it can contain only letters, digits, underscores, and hyphens, and must start with a letter. 
## Examples


Shows how to add a prefix that is prepended to all generated element IDs (svg).

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Id prefix.docx"));

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```
## Exceptions

* **ArgumentException** - The value does not meet the requirements specified above.

## See Also

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
