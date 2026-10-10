---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins طريقة"
linktitle: "get_PageMargins"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins طريقة. يحدد الهوامش حول الصفحات في مستند HTML. يتم قياس قيمة الهوامش بالنقاط ويجب أن تكون مساوية أو أكبر من 0. القيمة الافتراضية هي 10 نقاط في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.saving/htmlfixedsaveoptions/get_pagemargins/
---
## HtmlFixedSaveOptions::get_PageMargins method


يحدد الهوامش حول الصفحات في مستند HTML. تُقاس قيمة الهوامش بالنقاط ويجب أن تكون مساوية أو أكبر من 0. القيمة الافتراضية هي 10 نقاط.

```cpp
double Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins() const
```

## ملاحظات


يعتمد على قيمة الخاصية [PageHorizontalAlignment](../get_pagehorizontalalignment/):

* Defines top, bottom and left page margins if the value is [Left](../../htmlfixedpagehorizontalalignment/).
* Defines top, bottom and right page margins if the value is [Right](../../htmlfixedpagehorizontalalignment/).
* Defines top and bottom page margins if the value is [Center](../../htmlfixedpagehorizontalalignment/).



## أمثلة



يوضح كيفية تعديل هوامش الصفحة عند حفظ المستند إلى HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_PageMargins(15);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins/styles.css");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }")->get_Success());
```

## انظر أيضًا

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
