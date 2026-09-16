---
title: "Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf 方法"
linktitle: "get_SaveImagesAsWmf"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf 方法。当为 true 时，所有图像将在 C++ 中保存为 WMF。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.saving/rtfsaveoptions/get_saveimagesaswmf/
---
## RtfSaveOptions::get_SaveImagesAsWmf method


当 **true** 时，所有图像将保存为 WMF。

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf() const
```


## 示例



展示如何在将文档保存为 RTF 时，将文档中的所有图像转换为 Windows Metafile 格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jpeg image:");
System::SharedPtr<Aspose::Words::Drawing::Shape> imageShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, imageShape->get_ImageData()->get_ImageType());

builder->InsertParagraph();
builder->Writeln(u"Png image:");
imageShape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, imageShape->get_ImageData()->get_ImageType());

// 创建一个 \"RtfSaveOptions\" 对象并传递给文档的 \"Save\" 方法，以修改我们将其保存为 RTF 的方式。
auto rtfSaveOptions = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

// 将 "SaveImagesAsWmf" 属性设置为 "true"，以在将文档保存为 RTF 时将所有图像转换为 WMF。
// 这样做将帮助诸如 WordPad 等阅读器读取我们的文档。
// 将 "SaveImagesAsWmf" 属性设置为 "false"，以保留文档中所有图像的原始格式
// 在将其保存为 RTF 时。这将以牺牲对旧版 RTF 阅读器兼容性为代价，保留图像的质量。
rtfSaveOptions->set_SaveImagesAsWmf(saveImagesAsWmf);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.SaveImagesAsWmf.rtf", rtfSaveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"RtfSaveOptions.SaveImagesAsWmf.rtf");

System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

if (saveImagesAsWmf)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Wmf, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0)))->get_ImageData()->get_ImageType());
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Wmf, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0)))->get_ImageData()->get_ImageType());
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1)))->get_ImageData()->get_ImageType());
}
```

## 另见

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
