---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes 方法"
linktitle: "get_IgnoreFootnotes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes 方法。获取或设置一个布尔值，用于指示是否忽略脚注。默认值在 C++ 中为 false。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefootnotes/
---
## FindReplaceOptions::get_IgnoreFootnotes method


获取或设置一个布尔值，指示是否忽略脚注。默认值为 **false**。

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes() const
```


## 示例



展示如何在查找替换操作中忽略脚注。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder->InsertParagraph();

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// 将 "IgnoreFootnotes" 标志设置为 "true" 以进行查找替换
// 操作以忽略脚注中的文本。
// 将 "IgnoreFootnotes" 标志设置为 "false" 以进行查找替换
// 操作以同时搜索脚注中的文本。
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFootnotes(isIgnoreFootnotes);
doc->get_Range()->Replace(u"Lorem ipsum", u"Replaced Lorem ipsum", options);
```

## 另见

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
