---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted 方法"
linktitle: "get_IgnoreDeleted"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted 方法。获取或设置一个布尔值，指示是否忽略删除修订中的文本。默认值在 C++ 中为 false。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/get_ignoredeleted/
---
## FindReplaceOptions::get_IgnoreDeleted method


获取或设置一个布尔值，指示是否忽略删除修订中的文本。默认值为 **false**。

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted() const
```


## 示例



展示如何在查找替换操作期间包含或忽略删除修订中的文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// 开始跟踪修订并删除第二段，这将创建一个删除修订。
// 该段落将在文档中保留，直到我们接受删除修订。
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->Remove();
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsDeleteRevision());

// 我们可以使用 "FindReplaceOptions" 对象来修改查找和替换过程。
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// 将 "IgnoreDeleted" 标志设置为 "true" 以进行查找替换
// 操作将忽略属于删除修订的段落。
// 将 "IgnoreDeleted" 标志设置为 "false" 以进行查找替换
// 操作还将搜索删除修订中的文本。
options->set_IgnoreDeleted(ignoreTextInsideDeleteRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideDeleteRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## 另见

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
