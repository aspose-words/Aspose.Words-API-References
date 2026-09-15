---
title: "طريقة Aspose::Words::ConvertUtil::MillimeterToPoint"
linktitle: "MillimeterToPoint"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ConvertUtil::MillimeterToPoint. يحول المليمترات إلى نقاط في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil::MillimeterToPoint method


يحوّل المليمترات إلى نقاط.

```cpp
static double Aspose::Words::ConvertUtil::MillimeterToPoint(double millimeters)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| المليمترات | double | القيمة المراد تحويلها. |

## أمثلة



يعرض كيفية تحديد خصائص الصفحة بالمليمترات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تحدد "إعداد الصفحة" للقسم حجم هوامش الصفحة بالنقاط.
// يمكننا أيضًا استخدام الفئة "ConvertUtil" لاستخدام وحدة قياس أكثر مألوفة،
// مثل المليمترات عند تعريف الحدود.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(30));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(50));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(80));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(40));

// السنتيمتر الواحد يساوي تقريبًا 28.3 نقطة.
ASSERT_NEAR(28.34, Aspose::Words::ConvertUtil::MillimeterToPoint(10), 0.01);

// أضف محتوى لتوضيح الهوامش الجديدة.
builder->Writeln(System::String::Format(u"This Text is {0} points from the left, ", pageSetup->get_LeftMargin()) + System::String::Format(u"{0} points from the right, ", pageSetup->get_RightMargin()) + System::String::Format(u"{0} points from the top, ", pageSetup->get_TopMargin()) + System::String::Format(u"and {0} points from the bottom of the page.", pageSetup->get_BottomMargin()));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndMillimeters.docx");
```

## انظر أيضًا

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
