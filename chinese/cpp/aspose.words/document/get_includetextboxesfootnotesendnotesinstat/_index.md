---
title: "Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat 方法"
linktitle: "get_IncludeTextboxesFootnotesEndnotesInStat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat 方法。指定是否在 C++ 中的字数统计中包含文本框、脚注和尾注。"
type: docs
weight: 33000
url: /zh/cpp/aspose.words/document/get_includetextboxesfootnotesendnotesinstat/
---
## Document::get_IncludeTextboxesFootnotesEndnotesInStat method


指定是否在字数统计中包括文本框、脚注和尾注。

```cpp
bool Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat()
```


## 示例



展示如何在字数统计中包含或排除文本框、脚注和尾注。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Lorem ipsum");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"sit amet");

// 默认情况下，该选项设置为 'false'。
doc->UpdateWordCount();
// 不包含文本框、脚注和尾注的字数统计。
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Words());

doc->set_IncludeTextboxesFootnotesEndnotesInStat(true);
doc->UpdateWordCount();
// 包含文本框、脚注和尾注的字数统计。
ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Words());
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
