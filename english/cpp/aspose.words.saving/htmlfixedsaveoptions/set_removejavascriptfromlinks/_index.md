---
title: Aspose::Words::Saving::HtmlFixedSaveOptions::set_RemoveJavaScriptFromLinks method
linktitle: set_RemoveJavaScriptFromLinks
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlFixedSaveOptions::set_RemoveJavaScriptFromLinks method. Specifies whether JavaScript will be removed from links. Default is false in C++.'
type: docs
weight: 33500
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/set_removejavascriptfromlinks/
---
## HtmlFixedSaveOptions::set_RemoveJavaScriptFromLinks method


Specifies whether JavaScript will be removed from links. Default is **false**.

```cpp
void Aspose::Words::Saving::HtmlFixedSaveOptions::set_RemoveJavaScriptFromLinks(bool value)
```

## Remarks

 If this option is enabled, all links containing JavaScript (e.g., links with "javascript:" in the href attribute) will be replaced with "javascript:void(0)". This can help prevent potential security risks, such as XSS attacks. 
## Examples


Shows how to remove JavaScript from the links for html fixed documents.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"JavaScript in HREF.docx"));

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

Shows how to remove JavaScript from the links.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"JavaScript in HREF.docx"));

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```
## See Also

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
