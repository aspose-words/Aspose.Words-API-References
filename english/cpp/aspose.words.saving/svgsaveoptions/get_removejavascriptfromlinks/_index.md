---
title: Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks method
linktitle: get_RemoveJavaScriptFromLinks
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks method. Specifies whether JavaScript will be removed from links. Default is false. If this option is enabled, all links containing JavaScript will be replaced with "javascript:void(0)" in C++.'
type: docs
weight: 4750
url: /cpp/aspose.words.saving/svgsaveoptions/get_removejavascriptfromlinks/
---
## SvgSaveOptions::get_RemoveJavaScriptFromLinks method


Specifies whether JavaScript will be removed from links. Default is **false**. If this option is enabled, all links containing JavaScript will be replaced with "javascript:void(0)".

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## Examples



Shows how to remove JavaScript from the links (svg). 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

## See Also

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
