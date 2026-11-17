---
title: Aspose::Words::Saving::HtmlSaveOptions::set_RemoveJavaScriptFromLinks method
linktitle: set_RemoveJavaScriptFromLinks
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::set_RemoveJavaScriptFromLinks method. Specifies whether JavaScript will be removed from links. Default is false in C++.'
type: docs
weight: 88250
url: /cpp/aspose.words.saving/htmlsaveoptions/set_removejavascriptfromlinks/
---
## HtmlSaveOptions::set_RemoveJavaScriptFromLinks method


Specifies whether JavaScript will be removed from links. Default is **false**.

```cpp
void Aspose::Words::Saving::HtmlSaveOptions::set_RemoveJavaScriptFromLinks(bool value)
```

## Remarks

 If this option is enabled, all links containing JavaScript (e.g., links with "javascript:" in the href attribute) will be replaced with "javascript:void(0)". This can help prevent potential security risks, such as XSS attacks. 
## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
