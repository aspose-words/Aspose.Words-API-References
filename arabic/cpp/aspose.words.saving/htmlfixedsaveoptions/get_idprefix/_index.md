---
title: "طريقة Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix"
linktitle: "get_IdPrefix"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix. يحدد بادئة تُضاف إلى جميع معرفات العناصر المُولدة في المستند الناتج. القيمة الافتراضية هي null ولا تُضاف أي بادئة في C++."
type: docs
weight: 10500
url: /ar/cpp/aspose.words.saving/htmlfixedsaveoptions/get_idprefix/
---
## HtmlFixedSaveOptions::get_IdPrefix method


يحدد بادئة تُضاف إلى جميع معرّفات العناصر المُنشأة في المستند الناتج. القيمة الافتراضية هي null ولا تُضاف أي بادئة.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix() const
```


## أمثلة



يظهر كيفية إضافة بادئة تُضاف إلى جميع معرفات العناصر المُولدة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

## انظر أيضًا

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
