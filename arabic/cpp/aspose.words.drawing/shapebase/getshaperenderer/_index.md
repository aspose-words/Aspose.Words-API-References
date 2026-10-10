---
title: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer طريقة"
linktitle: "GetShapeRenderer"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer طريقة. ينشئ ويعيد كائنًا يمكن استخدامه لتصوير هذا الشكل إلى صورة في C++."
type: docs
weight: 58000
url: /ar/cpp/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase::GetShapeRenderer method


ينشئ ويعيد كائنًا يمكن استخدامه لتصوير هذا الشكل إلى صورة.

```cpp
System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> Aspose::Words::Drawing::ShapeBase::GetShapeRenderer()
```


### ReturnValue

كائن المُصوّر لهذا الشكل.
## ملاحظات


هذه الطريقة تستدعي فقط مُنشئ [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/) وتمرّر هذا الكائن كمعامل.

## أمثلة



يوضح كيفية استخدام مُصوّر الشكل لتصدير الأشكال إلى ملفات في نظام الملفات المحلي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// هناك 7 أشكال في المستند، بما في ذلك شكل مجموعة واحد يحتوي على شكلين فرعيين.
// سنقوم بتصوير كل شكل إلى ملف صورة في نظام الملفات المحلي
// مع تجاهل أشكال المجموعة لأنها لا تملك مظهرًا.
// سيؤدي هذا إلى إنتاج 6 ملفات صورة.
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## انظر أيضًا

* Class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
