---
title: "Aspose::Words::Drawing::ImageData::get_ImageType 方法"
linktitle: "get_ImageType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ImageData::get_ImageType 方法。获取 C++ 中图像的类型。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.drawing/imagedata/get_imagetype/
---
## ImageData::get_ImageType method


获取图像的类型。

```cpp
Aspose::Words::Drawing::ImageType Aspose::Words::Drawing::ImageData::get_ImageType()
```


## 示例



展示如何从文档中提取图像，并将它们保存为本地文件系统中的单独文件。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// 从文档中获取形状集合，
// 并将每个包含图像的形状的图像数据保存为本地文件系统中的文件。
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
        // 形状的图像数据可能包含多种可能的图像格式。
        // 我们可以根据图像的格式自动确定每个图像的文件扩展名。
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```

## 另见

* Enum [ImageType](../../imagetype/)
* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
