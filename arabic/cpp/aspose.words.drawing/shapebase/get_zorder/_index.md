---
title: "طريقة Aspose::Words::Drawing::ShapeBase::get_ZOrder"
linktitle: "get_ZOrder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::get_ZOrder. تحدد ترتيب عرض الأشكال المتداخلة في C++."
type: docs
weight: 57000
url: /ar/cpp/aspose.words.drawing/shapebase/get_zorder/
---
## ShapeBase::get_ZOrder method


يحدد ترتيب عرض الأشكال المتداخلة.

```cpp
int32_t Aspose::Words::Drawing::ShapeBase::get_ZOrder()
```

## ملاحظات


يؤثر فقط على الأشكال ذات المستوى الأعلى.

القيمة الافتراضية هي 0.

الرقم يمثل أولوية التراص. سيتم عرض الشكل الذي يملك رقمًا أعلى كما لو كان يتداخل (\"أمام\") الشكل الذي يملك رقمًا أقل.

ترتيب الأشكال المتداخلة مستقل بين الأشكال الموجودة في الترويسة والنص الرئيسي للمستند.

ترتيب عرض الأشكال الفرعية داخل مجموعة أشكال يحدده ترتيبها داخل المجموعة.

## أمثلة



يوضح كيفية تعديل ترتيب الأشكال.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج ثلاثة مستطيلات بألوان مختلفة تتداخل جزئيًا مع بعضها البعض.
// عند إدراج شكل يتداخل مع شكل آخر، تقوم Aspose.Words بوضع الشكل الأحدث فوق الشكل القديم.
// سيتداخل المستطيل الأخضر الفاتح مع المستطيل الأزرق الفاتح وسيغطيه جزئيًا،
// والمستطيل الأزرق الفاتح سيغطي المستطيل البرتقالي.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 150, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 150, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightGreen());

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

// خاصية \"ZOrder\" للشكل تحدد أولوية تراصه بين الأشكال المتداخلة الأخرى.
// إذا كان لدى شكلان متداخلان قيم \"ZOrder\" مختلفة،
// سيقوم Microsoft Word بوضع الشكل الذي يملك قيمة أعلى فوق الشكل الذي يملك قيمة أقل.
// قم بتعيين قيم \"ZOrder\" لأشكالنا لوضع المستطيل البرتقالي الأول فوق المستطيل الأزرق الفاتح الثاني
// والمستطيل الأزرق الفاتح الثاني فوق المستطيل الأخضر الفاتح الثالث.
// سيؤدي ذلك إلى عكس ترتيب تراصهم الأصلي.
shapes[0]->set_ZOrder(3);
shapes[1]->set_ZOrder(2);
shapes[2]->set_ZOrder(1);

doc->Save(get_ArtifactsDir() + u"Shape.ZOrder.docx");
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
