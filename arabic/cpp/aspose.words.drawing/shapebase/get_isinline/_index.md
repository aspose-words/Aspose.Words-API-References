---
title: "Aspose::Words::Drawing::ShapeBase::get_IsInline طريقة"
linktitle: "get_IsInline"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsInline طريقة. طريقة سريعة لتحديد ما إذا كان هذا الشكل موضعًا ضمن النص في C++."
type: docs
weight: 30000
url: /ar/cpp/aspose.words.drawing/shapebase/get_isinline/
---
## ShapeBase::get_IsInline method


طريقة سريعة لتحديد ما إذا كان هذا الشكل موضعًا داخل النص.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInline()
```

## ملاحظات


يؤثر فقط على الأشكال ذات المستوى الأعلى.

## أمثلة



يعرض كيفية تحديد ما إذا كان الشكل ضمن النص أو عائمًا.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي نوعان من التغليف التي قد تمتلكها الأشكال.
// 1 -  ضمن النص:
builder->Write(u"Hello world! ");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());
builder->Write(u" Hello again.");

// الشكل المضمن يقع داخل فقرة بين عناصر الفقرة الأخرى، مثل سلاسل النص.
// في Microsoft Word، يمكننا النقر وسحب الشكل إلى أي فقرة كما لو كان حرفًا.
// إذا كان الشكل كبيرًا، سيؤثر على تباعد الفقرات عموديًا.
// لا يمكننا نقل هذا الشكل إلى مكان لا يحتوي على فقرة.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::Inline, shape->get_WrapType());
ASSERT_TRUE(shape->get_IsInline());

// 2 -  عائم:
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

// شكل عائم ينتمي إلى الفقرة التي نُدرجه فيها،
// والتي يمكننا تحديدها برمز مرساة يظهر عندما ننقر على الشكل.
// إذا لم يكن للشكل رمز مرساة مرئي إلى يساره،
// سنحتاج إلى تمكين المراسي المرئية عبر "Options" -> "Display" -> "Object Anchors".
// في Microsoft Word، قد نقوم بالنقر الأيسر وسحب هذا الشكل بحرية إلى أي موقع.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, shape->get_WrapType());
ASSERT_FALSE(shape->get_IsInline());

doc->Save(get_ArtifactsDir() + u"Shape.IsInline.docx");
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
