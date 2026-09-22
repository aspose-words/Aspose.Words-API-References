---
title: "Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment method"
linktitle: "get_HorizontalAlignment"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment method. يحدد كيفية تموضع الشكل أفقيًا في C++."
type: docs
weight: 23000
url: /ar/cpp/aspose.words.drawing/shapebase/get_horizontalalignment/
---
## ShapeBase::get_HorizontalAlignment method


يحدد كيفية تموضع الشكل أفقيًا.

```cpp
Aspose::Words::Drawing::HorizontalAlignment Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment()
```

## ملاحظات


القيمة الافتراضية هي [None](../../horizontalalignment/).

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

* Enum [HorizontalAlignment](../../horizontalalignment/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
