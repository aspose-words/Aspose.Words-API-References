---
title: "Aspose::Words::ControlChar::Tab 方法"
linktitle: "制表符"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ControlChar::Tab 方法。制表符字符：\"\\x0009\" 或 \"\\t\" 在 C++ 中。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words/controlchar/tab/
---
## ControlChar::Tab method


制表符字符: "\x0009" 或 "\t"。

```cpp
static System::String & Aspose::Words::ControlChar::Tab()
```


## 示例



展示如何为制表位位置设置自定义间隔。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 将制表位设置为每 72 点（1 英寸）出现一次。
builder->get_Document()->set_DefaultTabStop(72);

// 每个制表符会将其后面的文本对齐到最近的下一个制表位位置。
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::Tab() + u"World!");
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::TabChar + u"World!");
```

## 另见

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
