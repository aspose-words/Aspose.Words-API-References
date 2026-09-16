---
title: "Aspose::Words::ChapterPageSeparator enum"
linktitle: "ChapterPageSeparator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ChapterPageSeparator 枚举。定义在 C++ 中出现在章节号和页码之间的分隔符字符。"
type: docs
weight: 84000
url: /zh/cpp/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enum


定义出现在章节号和页码之间的分隔符字符。

```cpp
enum class ChapterPageSeparator
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Hyphen | 0 | 冒号。 |
| Period | 1 | 句号。 |
| Colon | 2 | 冒号。 |
| EmDash | 3 | 一个强调的破折号。 |
| EnDash | 4 | 标准破折号。 |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
