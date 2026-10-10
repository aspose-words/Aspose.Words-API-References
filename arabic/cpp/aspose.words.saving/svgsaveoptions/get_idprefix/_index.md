---
title: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix طريقة"
linktitle: "get_IdPrefix"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix طريقة. يحدد بادئة تُضاف إلى جميع معرفات العناصر المُولدة في المستند الناتج. القيمة الافتراضية هي null ولا تُضاف أي بادئة في C++."
type: docs
weight: 4250
url: /ar/cpp/aspose.words.saving/svgsaveoptions/get_idprefix/
---
## SvgSaveOptions::get_IdPrefix method


يحدد بادئة تُضاف إلى جميع معرّفات العناصر المُنشأة في المستند الناتج. القيمة الافتراضية هي null ولا تُضاف أي بادئة.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix() const
```


## أمثلة



يوضح كيفية إضافة بادئة تُضاف إلى جميع معرفات العناصر المُولدة (svg).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

## انظر أيضًا

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
