---
title: "Aspose::Words::ConvertUtil::PointToInch طريقة"
linktitle: "PointToInch"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ConvertUtil::PointToInch طريقة. يحول النقاط إلى بوصات في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil::PointToInch method


يحوّل النقاط إلى بوصات.

```cpp
static double Aspose::Words::ConvertUtil::PointToInch(double points)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| نقاط | double | القيمة المراد تحويلها. |

## أمثلة



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
