---
title: "Aspose::Words::Drawing::ImageData::ToByteArray 方法"
linktitle: "ToByteArray"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ImageData::ToByteArray 方法。无论图像是存储的还是链接的，均返回图像字节（在 C++ 中）。"
type: docs
weight: 36000
url: /zh/cpp/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData::ToByteArray method


返回任意图像的字节，无论图像是存储的还是链接的。

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::ToByteArray()
```

## 备注


如果图像是链接的，每次调用时都会下载该图像。

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
