---
title: "Aspose::Words::Saving::PageSet 类"
linktitle: "PageSet"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PageSet 类。描述一组随机页面。要了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 20000
url: /zh/cpp/aspose.words.saving/pageset/
---
## PageSet class


描述一组随机页面。欲了解更多，请访问 [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) 文档文章。

```cpp
class PageSet : public System::Collections::Generic::IEnumerable<int32_t>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| static [get_All](./get_all/)() | 获取文档中所有页面的集合，保持原始顺序。 |
| static [get_Even](./get_even/)() | 获取文档中所有偶数页的集合，保持原始顺序。 |
| static [get_Odd](./get_odd/)() | 获取文档中所有奇数页的集合，保持原始顺序。 |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSet](./pageset/)(int32_t) | 基于精确的页面索引创建单页集合。 |
| [PageSet](./pageset/)(const System::ArrayPtr\<int32_t\>\&) | 基于精确的页面索引创建页面集合。 |
| [PageSet](./pageset/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) | 基于范围创建页面集合。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
