---
title: Aspose::Words::Saving::HtmlSaveOptions::get_RemoveJavaScriptFromLinks method
linktitle: get_RemoveJavaScriptFromLinks
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_RemoveJavaScriptFromLinks method. Specifies whether JavaScript will be removed from links. Default is false in C++.'
type: docs
weight: 49840
url: /cpp/aspose.words.saving/htmlsaveoptions/get_removejavascriptfromlinks/
---
## HtmlSaveOptions::get_RemoveJavaScriptFromLinks method


Specifies whether JavaScript will be removed from links. Default is **false**.

```cpp
_Bool Aspose::Words::Saving::HtmlSaveOptions::get_RemoveJavaScriptFromLinks() const
```

## Remarks

 If this option is enabled, all links containing JavaScript (e.g., links with "javascript:" in the href attribute) will be replaced with "javascript:void(0)". This can help prevent potential security risks, such as XSS attacks. 
## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
