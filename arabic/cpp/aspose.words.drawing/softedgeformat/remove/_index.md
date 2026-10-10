---
title: "طريقة Aspose::Words::Drawing::SoftEdgeFormat::Remove"
linktitle: "Remove"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::SoftEdgeFormat::Remove. يزيل SoftEdgeFormat من الكائن الأصل في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.drawing/softedgeformat/remove/
---
## SoftEdgeFormat::Remove method


يزيل [SoftEdgeFormat](../) من الكائن الأصل.

```cpp
void Aspose::Words::Drawing::SoftEdgeFormat::Remove()
```


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


يوضح كيفية تعيين حد لدقة الصورة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## انظر أيضًا

* Class [SoftEdgeFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
