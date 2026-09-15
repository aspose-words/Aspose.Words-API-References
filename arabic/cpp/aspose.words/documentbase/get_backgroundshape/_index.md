---
title: "طريقة Aspose::Words::DocumentBase::get_BackgroundShape"
linktitle: "get_BackgroundShape"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBase::get_BackgroundShape. تحصل على الشكل الخلفي للمستند أو تعينه. يمكن أن تكون القيمة null في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/documentbase/get_backgroundshape/
---
## DocumentBase::get_BackgroundShape method


يحصل أو يضبط شكل الخلفية للمستند. يمكن أن يكون **null**.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBase::get_BackgroundShape() const
```

## ملاحظات


يسمح Microsoft Word فقط بشكل يكون خاصية [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) الخاصة به مساوية لـ [Rectangle](../../../aspose.words.drawing/shapetype/) لاستخدامه كشكل خلفية لمستند.

يدعم Microsoft Word فقط خصائص التعبئة لشكل الخلفية. يتم تجاهل جميع الخصائص الأخرى.

ضبط هذه الخاصية على قيمة غير null سيؤدي أيضًا إلى تعيين [DisplayBackgroundShape](../../../aspose.words.settings/viewoptions/get_displaybackgroundshape/) إلى **true**.

## أمثلة



يظهر كيفية تعيين شكل خلفية لكل صفحة من المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_TRUE(System::TestTools::IsNull(doc->get_BackgroundShape()));

// نوع الشكل الوحيد الذي يمكننا استخدامه كخلفية هو المستطيل.
auto shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);

// هناك طريقتان لاستخدام هذا الشكل كخلفية للصفحة.
// 1 -  لون ثابت:
shapeRectangle->set_FillColor(System::Drawing::Color::get_LightBlue());
doc->set_BackgroundShape(shapeRectangle);

doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.FlatColor.docx");

// 2 -  صورة:
shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shapeRectangle->get_ImageData()->SetImage(get_ImageDir() + u"Transparent background logo.png");

// ضبط مظهر الصورة لجعلها أكثر ملاءمة كعلامة مائية.
shapeRectangle->get_ImageData()->set_Contrast(0.2);
shapeRectangle->get_ImageData()->set_Brightness(0.7);

doc->set_BackgroundShape(shapeRectangle);

ASSERT_TRUE(doc->get_BackgroundShape()->get_HasImage());

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
saveOptions->set_CacheBackgroundGraphics(false);

// Microsoft Word لا يدعم الأشكال التي تحتوي على صور كخلفيات،
// لكن لا يزال بإمكاننا رؤية هذه الخلفيات في صيغ حفظ أخرى مثل .pdf.
doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
