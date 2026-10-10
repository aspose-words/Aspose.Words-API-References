---
title: "Aspose::Words::Drawing::ImageData::get_ImageBytes 方法"
linktitle: "get_ImageBytes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ImageData::get_ImageBytes 方法。获取或设置存储在形状中的图像原始字节（在 C++ 中）。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.drawing/imagedata/get_imagebytes/
---
## ImageData::get_ImageBytes method


获取或设置存储在形状中的图像原始字节。

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::get_ImageBytes()
```

## 备注


将值设置为 **null** 或空数组将从形状中移除图像。

如果图像未存储在文档中（例如该图像可能是链接的），则返回 **null**。

## 示例



展示如何从形状的原始图像数据创建图像文件。
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imgShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_TRUE(imgShape->get_HasImage());

// ToByteArray() 返回存储在 ImageBytes 属性中的数组。
ASPOSE_ASSERT_EQ(imgShape->get_ImageData()->get_ImageBytes(), imgShape->get_ImageData()->ToByteArray());

// 将形状的图像数据保存为本地文件系统中的图像文件。
{
    System::SharedPtr<System::IO::Stream> imgStream = imgShape->get_ImageData()->ToStream();
    {
        auto outStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Drawing.GetDataFromImage.png", System::IO::FileMode::Create, System::IO::FileAccess::ReadWrite);
        imgStream->CopyTo(outStream);
    }
}
```

## 另见

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
