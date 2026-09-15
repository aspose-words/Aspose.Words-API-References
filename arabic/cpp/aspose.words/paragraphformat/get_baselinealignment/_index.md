---
title: "Aspose::Words::ParagraphFormat::get_BaselineAlignment طريقة"
linktitle: "get_BaselineAlignment"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphFormat::get_BaselineAlignment طريقة. يحصل على أو يضبط الموضع العمودي للخطوط على السطر في C++."
type: docs
weight: 5500
url: /ar/cpp/aspose.words/paragraphformat/get_baselinealignment/
---
## ParagraphFormat::get_BaselineAlignment method


يحصل أو يضبط الموضع العمودي للخطوط على السطر.

```cpp
Aspose::Words::BaselineAlignment Aspose::Words::ParagraphFormat::get_BaselineAlignment()
```


## أمثلة



يوضح كيفية ضبط الموضع الرأسي للخطوط على سطر.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();
if (format->get_BaselineAlignment() == Aspose::Words::BaselineAlignment::Auto)
{
    format->set_BaselineAlignment(Aspose::Words::BaselineAlignment::Top);
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphBaselineAlignment.docx");
```

## انظر أيضًا

* Enum [BaselineAlignment](../../baselinealignment/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
