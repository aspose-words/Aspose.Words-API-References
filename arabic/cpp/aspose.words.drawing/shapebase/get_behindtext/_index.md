---
title: "Aspose::Words::Drawing::ShapeBase::get_BehindText طريقة"
linktitle: "get_BehindText"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_BehindText طريقة. يحدد ما إذا كان الشكل أسفل أو أعلى النص في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.drawing/shapebase/get_behindtext/
---
## ShapeBase::get_BehindText method


يحدد ما إذا كان الشكل أسفل أو أعلى النص.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_BehindText()
```

## ملاحظات


يؤثر فقط على الأشكال ذات المستوى الأعلى.

القيمة الافتراضية هي **false**.

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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
