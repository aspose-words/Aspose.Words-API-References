---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly 方法"
linktitle: "get_FindWholeWordsOnly"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly 方法。True 表示 oldValue 必须是一个独立的单词（在 C++ 中）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/get_findwholewordsonly/
---
## FindReplaceOptions::get_FindWholeWordsOnly method


True 表示 oldValue 必须是一个独立的单词。

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly() const
```


## 示例



展示如何切换仅针对独立单词的查找替换操作。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// 我们可以使用 "FindReplaceOptions" 对象来修改查找替换过程。
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// 将 "FindWholeWordsOnly" 标志设置为 "true"，如果找到的文本不是其他单词的一部分，则进行替换。
// 将 "FindWholeWordsOnly" 标志设置为 "false"，无论其周围环境如何，都替换所有文本。
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## 另见

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
