---
title: "طريقة Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml"
linktitle: "get_SupportVml"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml. يحصل على أو يعيّن قيمة تشير إلى ما إذا كان يجب دعم صور VML في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.loading/htmlloadoptions/get_supportvml/
---
## HtmlLoadOptions::get_SupportVml method


يحصل أو يعيّن قيمة تشير إلى ما إذا كان يجب دعم صور VML.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml() const
```


## أمثلة



يظهر كيفية دعم التعليقات الشرطية أثناء تحميل مستند HTML.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// إذا كانت القيمة true، فإننا نأخذ شفرة VML في الاعتبار أثناء تحليل المستند المحمَّل.
loadOptions->set_SupportVml(supportVml);

// يحتوي هذا المستند على صورة JPEG داخل وسوم "<!--[if gte vml 1]>"،
// و صورة PNG مختلفة داخل وسوم "<![if !vml]>".
// إذا قمنا بتعيين العلامة "SupportVml" إلى "true"، فستقوم Aspose.Words بتحميل صورة JPEG.
// إذا قمنا بتعيين هذه العلامة إلى "false"، فستقوم Aspose.Words بتحميل صورة PNG فقط.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## انظر أيضًا

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
