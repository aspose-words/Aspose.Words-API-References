---
title: "Aspose::Words::Drawing::RelativeVerticalSize enum"
linktitle: "RelativeVerticalSize"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::RelativeVerticalSize enum. يحدد نسبيًا ما يتم حساب ارتفاع الشكل أو إطار النص عموديًا في C++."
type: docs
weight: 34500
url: /ar/cpp/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enum


يحدد نسبياً ما الذي يُحسب بناءً عليه ارتفاع الشكل أو إطار النص عمودياً.

```cpp
enum class RelativeVerticalSize
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| الهامش | 0 | يحدد أن الارتفاع يُحسب نسبيًا إلى المسافة بين الهامش العلوي والهامش السفلي. |
| Page | 1 | يحدد أن الارتفاع يُحسب نسبيًا إلى ارتفاع الصفحة. |
| TopMargin | 2 | يحدد أن الارتفاع يُحسب نسبيًا إلى حجم منطقة الهامش العلوي. |
| BottomMargin | 3 | يحدد أن الارتفاع يُحسب نسبيًا إلى حجم منطقة الهامش السفلي. |
| InnerMargin | 4 | يحدد أن الارتفاع يُحسب نسبيًا إلى حجم منطقة الهامش الداخلي، إلى حجم منطقة الهامش العلوي للصفحات الفردية وإلى حجم منطقة الهامش السفلي للصفحات الزوجية. |
| OuterMargin | 5 | يحدد أن الارتفاع يُحسب نسبيًا إلى حجم منطقة الهامش الخارجي، إلى حجم منطقة الهامش السفلي للصفحات الفردية وإلى حجم منطقة الهامش العلوي للصفحات الزوجية. |
| Default | n/a | القيمة الافتراضية هي [Margin](./). |


## أمثلة



يوضح كيفية ضبط الحجم النسبي والموضع.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إضافة شكل بسيط بحجم وموضع مطلق.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 40);
// اضبط WrapType إلى WrapType.None لأن الأشكال المضمنة يتم تحويلها تلقائيًا إلى وحدات مطلقة.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// التحقق وضبط الحجم الأفقي النسبي.
if (shape->get_RelativeHorizontalSize() == Aspose::Words::Drawing::RelativeHorizontalSize::Default)
{
    // ضبط ربط الحجم الأفقي إلى Margin.
    shape->set_RelativeHorizontalSize(Aspose::Words::Drawing::RelativeHorizontalSize::Margin);
    // ضبط العرض إلى 50٪ من عرض Margin.
    shape->set_WidthRelative(50.0f);
}

// التحقق وضبط الحجم العمودي النسبي.
if (shape->get_RelativeVerticalSize() == Aspose::Words::Drawing::RelativeVerticalSize::Default)
{
    // ضبط ربط الحجم العمودي إلى Margin.
    shape->set_RelativeVerticalSize(Aspose::Words::Drawing::RelativeVerticalSize::Margin);
    // ضبط الارتفاع إلى 30٪ من ارتفاع Margin.
    shape->set_HeightRelative(30.0f);
}

// التحقق وضبط الموضع العمودي النسبي.
if (shape->get_RelativeVerticalPosition() == Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph)
{
    // ضبط ربط الموضع إلى TopMargin.
    shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin);
    // ضبط Top النسبي إلى 30٪ من موضع TopMargin.
    shape->set_TopRelative(30.0f);
}

// التحقق وضبط الموضع الأفقي النسبي.
if (shape->get_RelativeHorizontalPosition() == Aspose::Words::Drawing::RelativeHorizontalPosition::Default)
{
    // ضبط ربط الموضع إلى RightMargin.
    shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin);
    // القيمة النسبية للموضع يمكن أن تكون سلبية.
    shape->set_LeftRelative(-260.0f);
}

doc->Save(get_ArtifactsDir() + u"Shape.RelativeSizeAndPosition.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
