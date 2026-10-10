---
title: "Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks Methode"
linktitle: "get_RemoveJavaScriptFromLinks"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks Methode. Gibt an, ob JavaScript aus Links entfernt wird. Standard ist false. Wenn diese Option aktiviert ist, werden alle Links, die JavaScript enthalten, durch \"javascript:void(0)\" in C++ ersetzt."
type: docs
weight: 4750
url: /de/cpp/aspose.words.saving/svgsaveoptions/get_removejavascriptfromlinks/
---
## SvgSaveOptions::get_RemoveJavaScriptFromLinks method


Gibt an, ob JavaScript aus Links entfernt wird. Standard ist **false**. Wenn diese Option aktiviert ist, werden alle Links, die JavaScript enthalten, durch \"javascript:void(0)\" ersetzt.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## Beispiele



Zeigt, wie JavaScript aus den Links (svg) entfernt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

## Siehe auch

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
