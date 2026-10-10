---
title: "Aspose::Words::PageSetup::get_HeadingLevelForChapter 方法"
linktitle: "get_HeadingLevelForChapter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_HeadingLevelForChapter 方法。获取或设置在 C++ 中应用于文档章节标题的标题级别样式。"
type: docs
weight: 20000
url: /zh/cpp/aspose.words/pagesetup/get_headinglevelforchapter/
---
## PageSetup::get_HeadingLevelForChapter method


获取或设置应用于文档章节标题的标题级别样式。

```cpp
int32_t Aspose::Words::PageSetup::get_HeadingLevelForChapter()
```

## 备注


可以是 0 到 9 之间的数字。0 表示如果应用于页码则没有章节编号。

在创建包含章节号的页码之前，文档标题必须应用编号大纲格式。

## 示例



展示如何使用页面章节。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_FirstSection()->get_PageSetup();

pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
pageSetup->set_ChapterPageSeparator(Aspose::Words::ChapterPageSeparator::Colon);
pageSetup->set_HeadingLevelForChapter(1);
```

## 另见

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
