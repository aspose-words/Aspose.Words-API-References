---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted 方法"
linktitle: "get_IgnoreInserted"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted 方法。获取或设置一个布尔值，用于指示是否忽略插入修订中的文本。默认值在 C++ 中为 false。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreinserted/
---
## FindReplaceOptions::get_IgnoreInserted method


获取或设置一个布尔值，指示是否忽略插入修订中的文本。默认值为 **false**。

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted() const
```


## 示例



展示如何在查找替换操作期间包含或忽略插入修订中的文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

// 开始跟踪修订并插入一个段落。该段落将成为插入修订。
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"Hello again!");
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsInsertRevision());

// 我们可以使用 "FindReplaceOptions" 对象来修改查找替换过程。
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// 将 \"IgnoreInserted\" 标志设置为 \"true\" 以进行查找替换
// 操作以忽略作为插入修订的段落。
// 将 \"IgnoreInserted\" 标志设置为 \"false\" 以进行查找替换
// 操作以同时搜索插入修订中的文本。
options->set_IgnoreInserted(ignoreTextInsideInsertRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideInsertRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## 另见

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
