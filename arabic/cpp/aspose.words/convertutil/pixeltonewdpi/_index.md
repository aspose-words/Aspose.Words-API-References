---
title: "Aspose::Words::ConvertUtil::PixelToNewDpi طريقة"
linktitle: "PixelToNewDpi"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ConvertUtil::PixelToNewDpi طريقة. يقوم بتحويل البكسلات من دقة إلى أخرى في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil::PixelToNewDpi method


يحوّل البكسلات من دقة إلى أخرى.

```cpp
static int32_t Aspose::Words::ConvertUtil::PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| بكسلات | double | القيمة المراد تحويلها. |
| oldDpi | double | دقة الـ dpi الحالية (نقاط لكل بوصة). |
| newDpi | double | دقة الـ dpi الجديدة (نقاط لكل بوصة). |

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
