---
title: "Aspose::Words::Drawing::ImageData::get_CropLeft 方法"
linktitle: "get_CropLeft"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ImageData::get_CropLeft 方法。定义在 C++ 中从左侧裁剪图片的比例。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.drawing/imagedata/get_cropleft/
---
## ImageData::get_CropLeft method


定义从左侧移除图片的比例。

```cpp
double Aspose::Words::Drawing::ImageData::get_CropLeft()
```

## 备注


裁剪量可以在 -1.0 到 1.0 之间。默认值为 0。请注意，值为 1 时将不显示任何图片。负值会导致图片从被裁剪的边缘向内挤压（图片与裁剪边缘之间的空白将由形状的填充颜色填充）。小于 1 的正值会使剩余的图片被拉伸以适应形状。

默认值为 0。

## 示例



展示如何编辑形状的图像数据。
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");
auto sourceShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

auto dstDoc = System::MakeObject<Aspose::Words::Document>();

// 从源文档导入一个形状并将其追加到第一段。
auto importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

// 导入的形状包含图像。我们可以通过 ImageData 对象访问图像的属性和原始数据。
System::SharedPtr<Aspose::Words::Drawing::ImageData> imageData = importedShape->get_ImageData();
imageData->set_Title(u"Imported Image");

ASSERT_TRUE(imageData->get_HasImage());

// 如果图像没有边框，其 ImageData 对象将把边框颜色定义为空。
ASSERT_EQ(4, imageData->get_Borders()->get_Count());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, imageData->get_Borders()->idx_get(0)->get_Color());

// 此图像未链接到本地文件系统中的其他形状或图像文件。
ASSERT_FALSE(imageData->get_IsLink());
ASSERT_FALSE(imageData->get_IsLinkOnly());

// “Brightness”（亮度）和 “Contrast”（对比度）属性定义图像的亮度和对比度
// 在 0-1 的比例上，默认值为 0.5。
imageData->set_Brightness(0.8);
imageData->set_Contrast(1.0);

// 上述亮度和对比度值导致图像出现大量白色。
// 我们可以使用 ChromaKey 属性选择一种颜色并将其替换为透明，例如白色。
imageData->set_ChromaKey(System::Drawing::Color::get_White());

// 再次导入源形状并将图像设置为单色。
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_GrayScale(true);

// 再次导入源形状以创建第三个图像并将其设置为 BiLevel。
// BiLevel 将每个像素设置为黑色或白色，以更接近原始颜色的那一种为准。
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_BiLevel(true);

// 裁剪在 0-1 的比例上确定。将一侧裁剪 0.3
// 将在裁剪的一侧裁掉 30% 的图像。
importedShape->get_ImageData()->set_CropBottom(0.3);
importedShape->get_ImageData()->set_CropLeft(0.3);
importedShape->get_ImageData()->set_CropTop(0.3);
importedShape->get_ImageData()->set_CropRight(0.3);

dstDoc->Save(get_ArtifactsDir() + u"Drawing.ImageData.docx");
```

## 另见

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
