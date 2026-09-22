---
title: "طريقة Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks"
linktitle: "get_RemoveJavaScriptFromLinks"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks. تحدد ما إذا كان سيتم إزالة JavaScript من الروابط. القيمة الافتراضية هي false. إذا تم تمكين هذا الخيار، سيتم استبدال جميع الروابط التي تحتوي على JavaScript بـ \"javascript:void(0)\" في C++."
type: docs
weight: 4750
url: /ar/cpp/aspose.words.saving/svgsaveoptions/get_removejavascriptfromlinks/
---
## SvgSaveOptions::get_RemoveJavaScriptFromLinks method


يحدد ما إذا كان سيتم إزالة JavaScript من الروابط. القيمة الافتراضية هي **false**. إذا تم تمكين هذا الخيار، سيتم استبدال جميع الروابط التي تحتوي على JavaScript بـ "javascript:void(0)".

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## أمثلة



يعرض كيفية إزالة JavaScript من الروابط (svg).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

## انظر أيضًا

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
