---
title: "Aspose::Words::Drawing::ImageData 类"
linktitle: "ImageData"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ImageData 类。定义形状的图像。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.drawing/imagedata/
---
## ImageData class


为形状定义图像。要了解更多信息，请访问 [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/) 文档文章。

```cpp
class ImageData : public Aspose::Words::IBorderAttrSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [FitImageToShape](./fitimagetoshape/)() | 将图像数据适配到 [Shape](../shape/) 框架，使图像数据的宽高比与 [Shape](../shape/) 框架的宽高比匹配。 |
| [get_BiLevel](./get_bilevel/)() | 确定图像是否以黑白方式显示。 |
| [get_Borders](./get_borders/)() | 获取图像的边框集合。边框仅对内联图像有效。 |
| [get_Brightness](./get_brightness/)() | 获取或设置图片的亮度。此属性的值必须是 0.0（最暗）到 1.0（最亮）之间的数字。 |
| [get_ChromaKey](./get_chromakey/)() | 定义将被视为透明的图像颜色值。 |
| [get_Contrast](./get_contrast/)() | 获取或设置指定图片的对比度。此属性的值必须是 0.0（最低对比度）到 1.0（最高对比度）之间的数字。 |
| [get_CropBottom](./get_cropbottom/)() | 定义从底部移除图片的比例。 |
| [get_CropLeft](./get_cropleft/)() | 定义从左侧移除图片的比例。 |
| [get_CropRight](./get_cropright/)() | 定义从右侧移除图片的比例。 |
| [get_CropTop](./get_croptop/)() | 定义从顶部移除图片的比例。 |
| [get_GrayScale](./get_grayscale/)() | 确定图片是否以灰度模式显示。 |
| [get_HasImage](./get_hasimage/)() | 如果形状具有图像字节或链接了图像，则返回 **true**。 |
| [get_ImageBytes](./get_imagebytes/)() | 获取或设置存储在形状中的图像原始字节。 |
| [get_ImageSize](./get_imagesize/)() | 获取有关图像尺寸和分辨率的信息。 |
| [get_ImageType](./get_imagetype/)() | 获取图像的类型。 |
| [get_IsLink](./get_islink/)() | 如果图像已链接到形状（当指定了 [SourceFullName](./get_sourcefullname/) 时），则返回 **true**。 |
| [get_IsLinkOnly](./get_islinkonly/)() | 如果图像已链接且未存储在文档中，则返回 **true**。 |
| [get_SourceFullName](./get_sourcefullname/)() | 获取或设置链接图像的源文件路径和名称。 |
| [get_Title](./get_title/)() | 定义图像的标题。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | 将图像保存到指定的流中。 |
| [Save](./save/)(const System::String\&) | 将图像保存到文件中。 |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_BiLevel](./set_bilevel/)(bool) | [Aspose::Words::Drawing::ImageData::get_BiLevel](./get_bilevel/) 的设置器。 |
| [set_Brightness](./set_brightness/)(double) | [Aspose::Words::Drawing::ImageData::get_Brightness](./get_brightness/) 的设置器。 |
| [set_ChromaKey](./set_chromakey/)(System::Drawing::Color) | [Aspose::Words::Drawing::ImageData::get_ChromaKey](./get_chromakey/) 的设置器。 |
| [set_Contrast](./set_contrast/)(double) | 用于设置 [Aspose::Words::Drawing::ImageData::get_Contrast](./get_contrast/) 的 setter。 |
| [set_CropBottom](./set_cropbottom/)(double) | 用于设置 [Aspose::Words::Drawing::ImageData::get_CropBottom](./get_cropbottom/) 的 setter。 |
| [set_CropLeft](./set_cropleft/)(double) | 用于设置 [Aspose::Words::Drawing::ImageData::get_CropLeft](./get_cropleft/) 的 setter。 |
| [set_CropRight](./set_cropright/)(double) | 用于设置 [Aspose::Words::Drawing::ImageData::get_CropRight](./get_cropright/) 的 setter。 |
| [set_CropTop](./set_croptop/)(double) | 用于设置 [Aspose::Words::Drawing::ImageData::get_CropTop](./get_croptop/) 的 setter。 |
| [set_GrayScale](./set_grayscale/)(bool) | 用于设置 [Aspose::Words::Drawing::ImageData::get_GrayScale](./get_grayscale/) 的 setter。 |
| [set_ImageBytes](./set_imagebytes/)(const System::ArrayPtr\<uint8_t\>\&) | 用于设置 [Aspose::Words::Drawing::ImageData::get_ImageBytes](./get_imagebytes/) 的 setter。 |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::ImageData::get_SourceFullName](./get_sourcefullname/) 的 setter。 |
| [set_Title](./set_title/)(const System::String\&) | 用于设置 [Aspose::Words::Drawing::ImageData::get_Title](./get_title/) 的 setter。 |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | 设置形状显示的图像。 |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | 设置形状显示的图像。 |
| [SetImage](./setimage/)(const System::String\&) | 设置形状显示的图像。 |
| [SetImage](./setimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [ToByteArray](./tobytearray/)() | 返回任意图像的字节，无论图像是存储的还是链接的。 |
| [ToImage](./toimage/)() | 获取以 **Image** 对象形式存储在形状中的图像。 |
| [ToStream](./tostream/)() | 创建并返回包含图像字节的流。 |
| static [Type](./type/)() |  |
## 备注


使用 [ImageData](../shape/get_imagedata/) 属性来访问和修改形状内部的图像。您不能直接创建 [ImageData](./) 类的实例。

图像可以存储在形状内部、链接到外部文件，或两者兼有（链接且存储在文档中）。

无论图像是存储在形状内部还是链接的，您都可以使用 [ToByteArray](./tobytearray/)、[ToStream](./tostream/)、[ToImage](./toimage/) 或 [Save()](../) 方法来访问实际图像。如果图像存储在形状内部，您也可以直接使用 [ImageBytes](./get_imagebytes/) 属性访问它。

要将图像存储在形状内部，请使用 [SetImage()](../) 方法。要将图像链接到形状，请设置 [SourceFullName](./get_sourcefullname/) 属性。

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
