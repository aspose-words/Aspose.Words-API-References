---
title: "Aspose::Words::Drawing::GradientStopCollection::idx_set طريقة"
linktitle: "idx_set"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::GradientStopCollection::idx_set طريقة. يحصل على أو يضبط كائن GradientStop في المجموعة في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.drawing/gradientstopcollection/idx_set/
---
## GradientStopCollection::idx_set method


تُحصل أو تُعيّن كائن [GradientStop](../../gradientstop/) في المجموعة.

```cpp
void Aspose::Words::Drawing::GradientStopCollection::idx_set(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::GradientStop> &value)
```


## أمثلة



يعرض كيفية إضافة نقاط تدرج إلى تعبئة التدرج.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
shape->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Green(), System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2);

// احصل على مجموعة نقاط التدرج.
System::SharedPtr<Aspose::Words::Drawing::GradientStopCollection> gradientStops = shape->get_Fill()->get_GradientStops();

// غيّر أول نقطة تدرج.
gradientStops->idx_get(0)->set_Color(System::Drawing::Color::get_Aqua());
gradientStops->idx_get(0)->set_Position(0.1);
gradientStops->idx_get(0)->set_Transparency(0.25);

// أضف نقطة تدرج جديدة إلى نهاية المجموعة.
auto gradientStop = System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Brown(), 0.5);
gradientStops->Add(gradientStop);

// أزل نقطة التدرج عند الفهرس 1.
gradientStops->RemoveAt(1);
// وأدرج نقطة تدرج جديدة عند نفس الفهرس 1.
gradientStops->Insert(1, System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Chocolate(), 0.75, 0.3));

// أزل آخر نقطة تدرج في المجموعة.
gradientStop = gradientStops->idx_get(2);
gradientStops->Remove(gradientStop);

ASSERT_EQ(2, gradientStops->get_Count());

ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 0, 255, 255), gradientStops->idx_get(0)->get_BaseColor());
ASSERT_EQ(System::Drawing::Color::get_Aqua().ToArgb(), gradientStops->idx_get(0)->get_Color().ToArgb());
ASSERT_NEAR(0.1, gradientStops->idx_get(0)->get_Position(), 0.01);
ASSERT_NEAR(0.25, gradientStops->idx_get(0)->get_Transparency(), 0.01);

ASSERT_EQ(System::Drawing::Color::get_Chocolate().ToArgb(), gradientStops->idx_get(1)->get_Color().ToArgb());
ASSERT_NEAR(0.75, gradientStops->idx_get(1)->get_Position(), 0.01);
ASSERT_NEAR(0.3, gradientStops->idx_get(1)->get_Transparency(), 0.01);

// استخدم خيار الامتثال لتعريف الشكل باستخدام DML
// إذا كنت تريد الحصول على الخاصية "GradientStops" بعد حفظ المستند.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientStops.docx", saveOptions);
```

## انظر أيضًا

* Class [GradientStop](../../gradientstop/)
* Class [GradientStopCollection](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
