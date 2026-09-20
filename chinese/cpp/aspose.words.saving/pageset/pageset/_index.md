---
title: "Aspose::Words::Saving::PageSet::PageSet 构造函数"
linktitle: "PageSet"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PageSet::PageSet 构造函数。根据 C++ 中的精确页面索引创建页面集合。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/pageset/pageset/
---
## PageSet::PageSet(const System::ArrayPtr\<int32_t\>\&) constructor


基于精确的页面索引创建页面集合。

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<int32_t> &pages)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 页面 | const System::ArrayPtr\<int32_t\>\& | 页面的零基索引。 |

## 示例



展示如何基于精确的页面索引提取页面。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 向文档添加五页。
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// 创建一个 "XpsSaveOptions" 对象，我们可以将其传递给文档的 "Save" 方法
// 以修改该方法将文档转换为 .XPS 的方式。
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// 使用 "PageSet" 属性选择文档的一组页面，以保存到输出 XPS。
// 在本例中，我们将通过零基索引选择仅三页：第 1 页、第 2 页和第 4 页。
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## 另见

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) constructor


基于范围创建页面集合。

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Saving::PageRange>> &ranges)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 范围 | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\& | 页面范围的数组。 |

## 示例



展示如何基于精确的页面范围提取页面。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## 另见

* Class [PageRange](../../pagerange/)
* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(int32_t) constructor


基于精确的页面索引创建单页集合。

```cpp
Aspose::Words::Saving::PageSet::PageSet(int32_t page)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 页面 | int32_t | 页面的零基索引。 |

## 示例



展示如何将文档中的单页渲染为 JPEG 图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// 创建一个 "ImageSaveOptions" 对象，以便将其传递给文档的 "Save" 方法。
// 以修改该方法将文档渲染为图像的方式。
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// 将 "PageSet" 设置为 "1" 以通过
// 零基索引来指定文档渲染的起始页。
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// 当我们将文档保存为 JPEG 格式时，Aspose.Words 只渲染一页。
// 此图像将包含从第二页开始的单页，
// 这将仅是原始文档的第二页。
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```

## 另见

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
