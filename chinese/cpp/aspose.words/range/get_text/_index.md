---
title: "Aspose::Words::Range::get_Text 方法"
linktitle: "get_Text"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Range::get_Text 方法。获取 C++ 中范围的文本。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/range/get_text/
---
## Range::get_Text method


获取范围的文本。

```cpp
System::String Aspose::Words::Range::get_Text()
```

## 备注


返回的字符串包含所有控制字符和特殊字符，如 [ControlChar](../../controlchar/) 中所述。

## 示例



展示如何获取范围覆盖的所有节点的文本内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## 另见

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
