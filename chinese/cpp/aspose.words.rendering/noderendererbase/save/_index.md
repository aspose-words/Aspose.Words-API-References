---
title: "Aspose::Words::Rendering::NodeRendererBase::Save 方法"
linktitle: "保存"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Rendering::NodeRendererBase::Save 方法。将形状渲染为图像并在 C++ 中保存到流中。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.rendering/noderendererbase/save/
---
## NodeRendererBase::Save(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method


将形状渲染为图像并保存到流。

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::SharedPtr<System::IO::Stream> &stream, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 流 | const System::SharedPtr\<System::IO::Stream\>\& | 用于保存形状图像的流。 |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\> | 指定控制形状渲染和保存方式的选项。可以为 **null**。如果为 **null**，图像将以 PNG 格式保存。 |

## 示例



展示如何使用形状渲染器将形状导出到本地文件系统中的文件。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// 文档中有 7 个形状，包括一个包含 2 个子形状的组合形状。
// 我们将在本地文件系统中将每个形状渲染为图像文件
// 同时忽略组合形状，因为它们没有外观。
// 这将生成 6 个图像文件。
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method


将形状渲染为 SVG 图像并保存到流。

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::SharedPtr<System::IO::Stream> &stream, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 流 | const System::SharedPtr\<System::IO::Stream\>\& | 用于保存形状 SVG 图像的流。 |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\> | 指定控制形状渲染和保存方式的选项。可以为 **null**。如果为 **null**，图像将使用默认选项保存。 |

## 示例



展示在渲染 Office Math 时如何传递保存选项。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"SvgSaveOptions.Output.svg", options);

{
    auto stream = System::MakeObject<System::IO::MemoryStream>();
    math->GetMathRenderer()->Save(stream, options);
}
```

## 另见

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method


将形状渲染为图像并保存到文件。

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::String &fileName, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 图像文件的名称。如果已存在具有指定名称的文件，则会覆盖现有文件。 |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\> | 指定控制形状渲染和保存方式的选项。可以为 **null**。 |

## 示例



展示如何将 Office [Math](../../../aspose.words.math/) 对象渲染为本地文件系统中的图像文件。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// 创建一个 "ImageSaveOptions" 对象，以传递给节点渲染器的 "Save" 方法进行修改。
// 它如何将 OfficeMath 节点渲染为图像。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// 将 "Scale" 属性设置为 5，以将对象渲染为原始大小的五倍。
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method


将形状渲染为 SVG 图像并保存到文件。

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::String &fileName, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 图像文件的名称。如果已存在具有指定名称的文件，则会覆盖现有文件。 |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\> | 指定控制形状渲染和保存方式的选项。可以为 **null**。 |

## 示例



展示在渲染 Office Math 时如何传递保存选项。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"SvgSaveOptions.Output.svg", options);

{
    auto stream = System::MakeObject<System::IO::MemoryStream>();
    math->GetMathRenderer()->Save(stream, options);
}
```

## 另见

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Rendering::NodeRendererBase::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```

## 另见

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Rendering::NodeRendererBase::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```

## 另见

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
