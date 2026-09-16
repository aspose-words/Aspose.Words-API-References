---
title: "Aspose::Words::PageSetup::get_ChapterPageSeparator 方法"
linktitle: "get_ChapterPageSeparator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_ChapterPageSeparator 方法。获取或设置在 C++ 中出现在章节号和页码之间的分隔符字符。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words/pagesetup/get_chapterpageseparator/
---
## PageSetup::get_ChapterPageSeparator method


获取或设置出现在章节号和页码之间的分隔符字符。

```cpp
Aspose::Words::ChapterPageSeparator Aspose::Words::PageSetup::get_ChapterPageSeparator()
```

## 备注


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

* Enum [ChapterPageSeparator](../../chapterpageseparator/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
