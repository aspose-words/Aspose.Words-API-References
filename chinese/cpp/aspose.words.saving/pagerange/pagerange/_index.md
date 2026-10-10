---
title: "Aspose::Words::Saving::PageRange::PageRange 构造函数"
linktitle: "PageRange"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PageRange::PageRange 构造函数。在 C++ 中创建一个新的页面范围对象。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.saving/pagerange/pagerange/
---
## PageRange::PageRange constructor


创建一个新的页面范围对象。

```cpp
Aspose::Words::Saving::PageRange::PageRange(int32_t from, int32_t to)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 从 | int32_t | 起始页的零基索引。 |
| 至 | int32_t | 结束页的零基索引。如果超过文档中最后一页的索引，则在渲染时会被截断以适应文档。 |

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

* Class [PageRange](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
