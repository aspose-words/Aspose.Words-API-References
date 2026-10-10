---
title: "طريقة Aspose::Words::Drawing::Shape::get_ImageData"
linktitle: "get_ImageData"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Shape::get_ImageData. توفر الوصول إلى صورة الشكل. تُرجع null إذا كان لا يمكن للشكل أن يحتوي على صورة في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.drawing/shape/get_imagedata/
---
## Shape::get_ImageData method


يوفر الوصول إلى صورة الشكل. يعيد **null** إذا لم يستطع الشكل أن يحتوي على صورة.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ImageData> Aspose::Words::Drawing::Shape::get_ImageData()
```


## أمثلة



يوضح كيفية استخراج الصور من مستند، وحفظها على نظام الملفات المحلي كملفات منفصلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// احصل على مجموعة الأشكال من المستند،
// واحفظ بيانات الصورة لكل شكل يحتوي على صورة كملف على نظام الملفات المحلي.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> s)>>([](System::SharedPtr<Aspose::Words::Node> s) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Drawing::Shape>(s))->get_HasImage();
}))));

int32_t imageIndex = 0;
for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        // قد تحتوي بيانات الصور للأشكال على صور بعدة تنسيقات صورة محتملة.
        // يمكننا تحديد امتداد الملف لكل صورة تلقائيًا بناءً على تنسيقها.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


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

* Class [ImageData](../../imagedata/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
