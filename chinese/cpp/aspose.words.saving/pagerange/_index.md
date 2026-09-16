---
title: "Aspose::Words::Saving::PageRange 类"
linktitle: "PageRange"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PageRange 类。表示连续的页面范围。要了解更多信息，请访问 C++ 中的文档文章。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words.saving/pagerange/
---
## PageRange class


表示连续的页面范围。欲了解更多，请访问 [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) 文档文章。

```cpp
class PageRange : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageRange](./pagerange/)(int32_t, int32_t) | 创建一个新的页面范围对象。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
