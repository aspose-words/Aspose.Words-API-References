---
title: Aspose::Words::Saving::SvgSaveOptions::set_RemoveJavaScriptFromLinks method
linktitle: set_RemoveJavaScriptFromLinks
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SvgSaveOptions::set_RemoveJavaScriptFromLinks method. Specifies whether JavaScript will be removed from links. Default is false. If this option is enabled, all links containing JavaScript will be replaced with "javascript:void(0)" in C++.'
type: docs
weight: 14750
url: /cpp/aspose.words.saving/svgsaveoptions/set_removejavascriptfromlinks/
---
## SvgSaveOptions::set_RemoveJavaScriptFromLinks method


Specifies whether JavaScript will be removed from links. Default is **false**. If this option is enabled, all links containing JavaScript will be replaced with "javascript:void(0)".

```cpp
void Aspose::Words::Saving::SvgSaveOptions::set_RemoveJavaScriptFromLinks(bool value)
```

## Examples


Shows how to remove JavaScript from the links (svg).

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"JavaScript in HREF.docx"));

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```
## See Also

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
