---
title: "طريقة Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition"
linktitle: "get_RelativeVerticalPosition"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition. تحدد ما إلى أي شيء يتم وضع الشكل عموديًا في C++."
type: docs
weight: 43000
url: /ar/cpp/aspose.words.drawing/shapebase/get_relativeverticalposition/
---
## ShapeBase::get_RelativeVerticalPosition method


يحدد بالنسبة إلى ماذا يتم تموضع الشكل عموديًا.

```cpp
Aspose::Words::Drawing::RelativeVerticalPosition Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition()
```

## ملاحظات


القيمة الافتراضية هي [Paragraph](../../relativeverticalposition/).

يؤثر فقط على الأشكال العائمة ذات المستوى الأعلى.

## أمثلة



يوضح كيفية إدراج صورة عائمة في مركز الصفحة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج صورة عائمة ستظهر خلف النص المتداخل ووازنها إلى مركز الصفحة.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## انظر أيضًا

* Enum [RelativeVerticalPosition](../../relativeverticalposition/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
