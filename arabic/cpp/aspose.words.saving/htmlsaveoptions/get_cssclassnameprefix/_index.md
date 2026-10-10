---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix طريقة"
linktitle: "get_CssClassNamePrefix"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix طريقة. تحدد بادئة تُضاف إلى جميع أسماء فئات CSS. القيمة الافتراضية هي سلسلة فارغة ولا تحتوي أسماء فئات CSS المُولدة على بادئة مشتركة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_cssclassnameprefix/
---
## HtmlSaveOptions::get_CssClassNamePrefix method


يحدد بادئة تُضاف إلى جميع أسماء فئات CSS. القيمة الافتراضية هي سلسلة فارغة ولا تحتوي أسماء فئات CSS المُولدة على أي بادئة مشتركة.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix() const
```

## ملاحظات


إذا لم تكن هذه القيمة فارغة، فستبدأ جميع فئات CSS التي يولدها Aspose.Words بالبادئة المحددة. قد يكون ذلك مفيدًا، على سبيل المثال، إذا قمت بإضافة CSS مخصص إلى المستندات المولدة وتريد منع تعارض أسماء الفئات.

إذا لم تكن القيمة **null** أو فارغة، يجب أن تكون معرف CSS صالح.

## أمثلة



يوضح كيفية حفظ مستند إلى HTML، وإضافة بادئة إلى جميع أسماء فئات CSS الخاصة به.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
saveOptions->set_CssClassNamePrefix(u"myprefix-");

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html");

ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Header\">"));
ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Footer\">"));

outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.css");

ASSERT_TRUE(outDocContents.Contains(u".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
ASSERT_TRUE(outDocContents.Contains(u".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
