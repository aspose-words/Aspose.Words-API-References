---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields 方法"
linktitle: "get_IgnoreFields"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields 方法。获取或设置一个布尔值，指示是否忽略字段内的文本。默认值在 C++ 中为 false。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefields/
---
## FindReplaceOptions::get_IgnoreFields method


获取或设置一个布尔值，指示是否忽略字段中的文本。默认值为 **false**。

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields() const
```

## 备注


此选项影响整个字段（所有位于 [FieldStart](../../../aspose.words/nodetype/) 和 [FieldEnd](../../../aspose.words/nodetype/) 之间的节点）。

若只想忽略字段代码，请使用相应的选项 [IgnoreFieldCodes](../get_ignorefieldcodes/)。

## 示例



展示如何忽略字段内的文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertField(u"QUOTE", u"Hello again!");

// 我们可以使用 "FindReplaceOptions" 对象来修改查找替换过程。
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// 将 "IgnoreFields" 标志设置为 "true" 以获取查找和替换
// 操作，以忽略字段内的文本。
// 将 "IgnoreFields" 标志设置为 "false" 以获取查找和替换
// 操作，以便也搜索字段内的文本。
options->set_IgnoreFields(ignoreTextInsideFields);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideFields ? System::String(u"Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015") : System::String(u"Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015"), doc->GetText().Trim());
```

## 另见

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
