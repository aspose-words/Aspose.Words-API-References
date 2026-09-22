---
title: "طريقة Aspose::Words::ConvertUtil::InchToPoint"
linktitle: "InchToPoint"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ConvertUtil::InchToPoint. يحول البوصات إلى نقاط في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words/convertutil/inchtopoint/
---
## ConvertUtil::InchToPoint method


يحوّل البوصات إلى نقاط.

```cpp
static double Aspose::Words::ConvertUtil::InchToPoint(double inches)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| البوصات | double | القيمة المراد تحويلها. |

## أمثلة



يظهر كيفية تعديل حجم الورق، الاتجاه، الهوامش، بالإضافة إلى إعدادات أخرى لقسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```


يظهر كيفية تحديد خصائص الصفحة بالبوصات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تحدد "إعداد الصفحة" للقسم حجم هوامش الصفحة بالنقاط.
// يمكننا أيضًا استخدام الفئة "ConvertUtil" لاستخدام وحدة قياس أكثر مألوفة،
// مثل البوصات عند تعريف الحدود.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(2.0));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(2.5));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));

// البوصة واحدة تساوي 72 نقطة.
ASPOSE_ASSERT_EQ(72.0, Aspose::Words::ConvertUtil::InchToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToInch(72));

// أضف محتوى لتوضيح الهوامش الجديدة.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} inches from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} inches from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} inches from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} inches from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndInches.docx");
```

## انظر أيضًا

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
