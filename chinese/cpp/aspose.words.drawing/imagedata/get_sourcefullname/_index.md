---
title: "Aspose::Words::Drawing::ImageData::get_SourceFullName 方法"
linktitle: "get_SourceFullName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ImageData::get_SourceFullName 方法。获取或设置链接图像的源文件的路径和名称（在 C++ 中）。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words.drawing/imagedata/get_sourcefullname/
---
## ImageData::get_SourceFullName method


获取或设置链接图像的源文件路径和名称。

```cpp
System::String Aspose::Words::Drawing::ImageData::get_SourceFullName()
```

## 备注


默认值为空字符串。

如果 [SourceFullName](./) 不是空字符串，则图像为链接状态。

## 示例



展示如何在文档中插入链接图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFileName = get_ImageDir() + u"Windows MetaFile.wmf";

// 下面是将图像应用于形状以便显示的两种方法。
// 1 - 将形状设置为包含图像。
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->SetImage(imageFileName);

builder->InsertNode(shape);

doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx");

// 我们在形状中存储的每个图像都会增加文档的大小。
ASSERT_TRUE(70000 < System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx")->get_Length());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->RemoveAllChildren();

// 2 -  将形状设置为链接到本地文件系统中的图像文件。
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->set_SourceFullName(imageFileName);

builder->InsertNode(shape);
doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx");

// 链接图像可以节省空间并使文档更小。
// 然而，文档只能在
// 图像文件位于形状的 "SourceFullName" 属性指向的位置时。
ASSERT_TRUE(10000 > System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx")->get_Length());
```

## 另见

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
