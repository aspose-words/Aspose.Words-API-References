---
title: "Aspose::Words::Drawing::ImageData::ToStream 方法"
linktitle: "ToStream"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ImageData::ToStream 方法。创建并返回一个包含图像字节的流（在 C++ 中）。"
type: docs
weight: 38000
url: /zh/cpp/aspose.words.drawing/imagedata/tostream/
---
## ImageData::ToStream method


创建并返回包含图像字节的流。

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Drawing::ImageData::ToStream()
```

## 备注


如果图像字节存储在形状中，则创建并返回一个 **MemoryStream** 对象。

如果图像是链接的并且存储在文件中，则打开该文件并返回一个 **FileStream** 对象。

如果图像是链接的并且存储在外部 URL 中，则下载该文件并返回一个 **MemoryStream** 对象。

是否由调用者负责释放流对象。

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
