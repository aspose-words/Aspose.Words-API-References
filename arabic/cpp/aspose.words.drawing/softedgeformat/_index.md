---
title: "Aspose::Words::Drawing::SoftEdgeFormat class"
linktitle: "SoftEdgeFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::SoftEdgeFormat class. يمثل تنسيق الحافة الناعمة لكائن في C++."
type: docs
weight: 13500
url: /ar/cpp/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class


يمثل تنسيق الحافة الناعمة لكائن.

```cpp
class SoftEdgeFormat : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Radius](./get_radius/)() | يحصل أو يعيّن قيمة مزدوجة تمثل طول نصف القطر لتأثير الحافة الناعمة بالنقاط (pt). القيمة الافتراضية هي 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | يزيل [SoftEdgeFormat](./) من الكائن الأب. |
| [set_Radius](./set_radius/)(double) | مُعيّن لـ [Aspose::Words::Drawing::SoftEdgeFormat::get_Radius](./get_radius/). |
| static [Type](./type/)() |  |
## ملاحظات


استخدم الخاصية [SoftEdge](../shapebase/get_softedge/) للوصول إلى خصائص الحافة الناعمة لكائن. لا تقوم بإنشاء مثيلات من الفئة [SoftEdgeFormat](./) مباشرة.

## أمثلة



يظهر كيفية العمل مع تنسيق الحافة الناعمة.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 200);

// تطبيق الحافة الناعمة على الشكل.
shape->get_SoftEdge()->set_Radius(30);

builder->get_Document()->Save(get_ArtifactsDir() + u"Shape.SoftEdge.docx");

// تحميل مستند يحتوي على شكل مستطيل مع حافة ناعمة.
auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.SoftEdge.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> softEdgeFormat = shape->get_SoftEdge();

// تحقق من نصف قطر الحافة الناعمة.
ASPOSE_ASSERT_EQ(30, softEdgeFormat->get_Radius());

// إزالة الحافة الناعمة من الشكل.
softEdgeFormat->Remove();

// تحقق من نصف قطر الحافة الناعمة التي تمت إزالتها.
ASPOSE_ASSERT_EQ(0, softEdgeFormat->get_Radius());
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
