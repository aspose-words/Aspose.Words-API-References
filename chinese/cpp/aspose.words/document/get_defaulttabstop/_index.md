---
title: "Aspose::Words::Document::get_DefaultTabStop 方法"
linktitle: "get_DefaultTabStop"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_DefaultTabStop 方法。获取或设置 C++ 中默认制表位之间的间隔（以点为单位）。"
type: docs
weight: 20000
url: /zh/cpp/aspose.words/document/get_defaulttabstop/
---
## Document::get_DefaultTabStop method


获取或设置默认制表位之间的间隔（以点为单位）。

```cpp
double Aspose::Words::Document::get_DefaultTabStop()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
