---
title: "Aspose::Words::ConvertUtil::PixelToPoint طريقة"
linktitle: "PixelToPoint"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ConvertUtil::PixelToPoint طريقة. يحول البكسلات إلى نقاط عند DPI 96 في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/convertutil/pixeltopoint/
---
## ConvertUtil::PixelToPoint(double) method


يحوّل البكسلات إلى نقاط عند 96 dpi.

```cpp
static double Aspose::Words::ConvertUtil::PixelToPoint(double pixels)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| بكسلات | double | القيمة المراد تحويلها. |

## أمثلة



يعرض كيفية تحديد خصائص الصفحة بالبكسل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تحدد "إعداد الصفحة" للقسم حجم هوامش الصفحة بالنقاط.
// يمكننا أيضًا استخدام الفئة "ConvertUtil" لاستخدام وحدة قياس مختلفة،
// مثل البكسلات عند تعريف الحدود.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::PixelToPoint(200));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::PixelToPoint(225));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::PixelToPoint(125));

// البكسل الواحد يساوي 0.75 نقطة.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToPixel(0.75));

// قيمة DPI الافتراضية المستخدمة هي 96.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1, 96));

// أضف محتوى لتوضيح الهوامش الجديدة.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} pixels from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} pixels from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} pixels from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} pixels from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixels.docx");
```

## انظر أيضًا

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## ConvertUtil::PixelToPoint(double, double) method


يحوّل البكسلات إلى نقاط عند دقة البكسل المحددة.

```cpp
static double Aspose::Words::ConvertUtil::PixelToPoint(double pixels, double resolution)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| بكسلات | double | القيمة المراد تحويلها. |
| الدقة | double | دقة الـ dpi (النقاط في البوصة). |

## أمثلة



يوضح كيفية تحويل النقاط إلى بكسلات باستخدام الدقة الافتراضية والمخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حدد حجم الهامش العلوي لهذا القسم بالبكسلات، وفقًا لـ DPI مخصص.
const double myDpi = 192;

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100, myDpi));

ASSERT_NEAR(37.5, pageSetup->get_TopMargin(), 0.01);

// عند DPI الافتراضي 96، البكسل يساوي 0.75 نقطة.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));

builder->Writeln(System::String::Format(u"This Text is {0} points/{1} ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + System::String::Format(u"pixels (at a DPI of {0}) from the top of the page.", myDpi));

// قم بتعيين DPI جديد واضبط قيمة الهامش العلوي وفقًا لذلك.
const double newDpi = 300;
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToNewDpi(pageSetup->get_TopMargin(), myDpi, newDpi));
ASSERT_NEAR(59.0, pageSetup->get_TopMargin(), 0.01);

builder->Writeln(System::String::Format(u"At a DPI of {0}, the text is now {1} points/{2} ", newDpi, pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + u"pixels from the top of the page.");

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixelsDpi.docx");
```

## انظر أيضًا

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
