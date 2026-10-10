---
title: "طريقة Aspose::Words::Drawing::ImageData::get_ImageType"
linktitle: "get_ImageType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ImageData::get_ImageType. يحصل على نوع الصورة في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.drawing/imagedata/get_imagetype/
---
## ImageData::get_ImageType method


يحصل على نوع الصورة.

```cpp
Aspose::Words::Drawing::ImageType Aspose::Words::Drawing::ImageData::get_ImageType()
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

## انظر أيضًا

* Enum [ImageType](../../imagetype/)
* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
