---
title: "Aspose::Words::Drawing::ShapeBase::get_DistanceBottom method"
linktitle: "get_DistanceBottom"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_DistanceBottom method. يُرجع أو يعيّن المسافة (بالنقاط) بين نص المستند والحافة السفلية للشكل في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.drawing/shapebase/get_distancebottom/
---
## ShapeBase::get_DistanceBottom method


يرجع أو يضبط المسافة (بالنقاط) بين نص المستند والحافة السفلية للشكل.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_DistanceBottom()
```

## ملاحظات


القيمة الافتراضية هي 0.

يؤثر فقط على الأشكال ذات المستوى الأعلى.

## أمثلة



يظهر كيفية تعيين مسافة الالتفاف لنص يحيط بشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج مستطيلًا، واحصل على النص ليلتف بإحكام حول حدوده.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 150, 150);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Tight);

// عيّن الحد الأدنى للمسافة بين الشكل والنص المحيط إلى 40 نقطة من جميع الجوانب.
shape->set_DistanceTop(40);
shape->set_DistanceBottom(40);
shape->set_DistanceLeft(40);
shape->set_DistanceRight(40);

// حرك الشكل أقرب إلى مركز الصفحة، ثم قم بتدوير الشكل 60 درجة باتجاه عقارب الساعة.
shape->set_Top(75);
shape->set_Left(150);
shape->set_Rotation(60);

// أضف نصًا سيلتف حول الشكل.
builder->get_Font()->set_Size(24);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"Shape.Coordinates.docx");
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
