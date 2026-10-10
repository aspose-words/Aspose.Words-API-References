---
title: "فئة Aspose::Words::Drawing::GradientStopCollection"
linktitle: "GradientStopCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Drawing::GradientStopCollection. تحتوي على مجموعة من كائنات GradientStop. لمعرفة المزيد، قم بزيارة مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.drawing/gradientstopcollection/
---
## GradientStopCollection class


تحتوي على مجموعة من كائنات [GradientStop](../gradientstop/). لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class GradientStopCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::GradientStop>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | يضيف [GradientStop](../gradientstop/) المحدد إلى تدرج لوني. |
| [get_Count](./get_count/)() | يحصل على قيمة عددية تشير إلى عدد العناصر في المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع عدّادًا يتنقل عبر المجموعة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يحصل أو يعيّن كائن [GradientStop](../gradientstop/) في المجموعة. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | يحصل أو يعيّن كائن [GradientStop](../gradientstop/) في المجموعة. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | يدرج [GradientStop](../gradientstop/) إلى المجموعة عند فهرس محدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | يزيل [GradientStop](../gradientstop/) المحدد من المجموعة. |
| [RemoveAt](./removeat/)(int32_t) | يزيل [GradientStop](../gradientstop/) من المجموعة عند فهرس محدد. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
