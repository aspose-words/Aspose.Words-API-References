---
title: "Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks metod"
linktitle: "get_RemoveJavaScriptFromLinks"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks metod. Anger om JavaScript ska tas bort från länkar. Standard är falskt. Om detta alternativ är aktiverat ersätts alla länkar som innehåller JavaScript med \"javascript:void(0)\" i C++."
type: docs
weight: 4750
url: /sv/cpp/aspose.words.saving/svgsaveoptions/get_removejavascriptfromlinks/
---
## SvgSaveOptions::get_RemoveJavaScriptFromLinks method


Anger om JavaScript ska tas bort från länkar. Standard är **false**. Om detta alternativ är aktiverat ersätts alla länkar som innehåller JavaScript med "javascript:void(0)".

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## Exempel



Visar hur man tar bort JavaScript från länkarna (svg).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

## Se även

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
