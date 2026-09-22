---
title: "طريقة Aspose::Words::DocumentBuilder::InsertNode"
linktitle: "InsertNode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::InsertNode. تُدرج عقدة قبل المؤشر في C++."
type: docs
weight: 40000
url: /ar/cpp/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder::InsertNode method


يقوم بإدراج عقدة قبل المؤشر.

```cpp
void Aspose::Words::DocumentBuilder::InsertNode(const System::SharedPtr<Aspose::Words::Node> &node)
```


## أمثلة



يوضح كيفية إدراج صورة مرتبطة في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFileName = get_ImageDir() + u"Windows MetaFile.wmf";

// فيما يلي طريقتان لتطبيق صورة على شكل بحيث يمكنه عرضها.
// 1 -  اضبط الشكل ليحتوي على الصورة.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->SetImage(imageFileName);

builder->InsertNode(shape);

doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx");

// كل صورة نقوم بتخزينها في الشكل ستزيد من حجم مستندنا.
ASSERT_TRUE(70000 < System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx")->get_Length());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->RemoveAllChildren();

// 2 -  اضبط الشكل ليرتبط بملف صورة في نظام الملفات المحلي.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->set_SourceFullName(imageFileName);

builder->InsertNode(shape);
doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx");

// ربط الصور سيوفر مساحة ويؤدي إلى مستند أصغر.
// مع ذلك، لا يمكن للمستند عرض الصورة بشكل صحيح إلا بينما
// ملف الصورة موجود في الموقع الذي تشير إليه خاصية "SourceFullName" للشكل.
ASSERT_TRUE(10000 > System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx")->get_Length());
```

## انظر أيضًا

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
