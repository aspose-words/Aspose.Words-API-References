---
title: "Aspose::Words::Saving::PageSavingArgs 类"
linktitle: "PageSavingArgs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PageSavingArgs 类。提供 PageSaving() 事件的数据。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 19000
url: /zh/cpp/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class


为 [PageSaving()](../ipagesavingcallback/pagesaving/) 事件提供数据。要了解更多，请访问 [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) 文档文章。

```cpp
class PageSavingArgs : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_KeepPageStreamOpen](./get_keeppagestreamopen/)() const | 指定 Aspose.Words 在保存文档页面后是保持流打开还是关闭。 |
| [get_PageFileName](./get_pagefilename/)() const | 获取文档页面将保存到的文件名。 |
| [get_PageIndex](./get_pageindex/)() const | 当前页面索引。 |
| [get_PageStream](./get_pagestream/)() const | 允许指定文档页面将保存到的流。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSavingArgs](./pagesavingargs/)() |  |
| [set_KeepPageStreamOpen](./set_keeppagestreamopen/)(bool) | 用于设置 [Aspose::Words::Saving::PageSavingArgs::get_KeepPageStreamOpen](./get_keeppagestreamopen/) 的 setter。 |
| [set_PageFileName](./set_pagefilename/)(const System::String\&) | 设置文档页面将保存到的文件名。 |
| [set_PageStream](./set_pagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | 用于设置 [Aspose::Words::Saving::PageSavingArgs::get_PageStream](./get_pagestream/) 的 setter。 |
| [set_PageStream](./set_pagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
