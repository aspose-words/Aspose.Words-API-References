---
title: "Aspose::Words::Document::RemoveMacros 方法"
linktitle: "RemoveMacros"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::RemoveMacros 方法。在 C++ 中从文档中移除所有宏（VBA 项目）以及工具栏和命令自定义。"
type: docs
weight: 69000
url: /zh/cpp/aspose.words/document/removemacros/
---
## Document::RemoveMacros method


从文档中删除所有宏（VBA 项目）以及工具栏和命令自定义。

```cpp
void Aspose::Words::Document::RemoveMacros()
```

## 备注


通过从文档中移除所有宏，您可以确保文档不包含宏病毒。

## 示例



展示如何从文档中移除所有宏。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");

ASSERT_TRUE(doc->get_HasMacros());
ASSERT_EQ(u"Project", doc->get_VbaProject()->get_Name());

// 移除文档的 VBA 项目以及所有宏。
doc->RemoveMacros();

ASSERT_FALSE(doc->get_HasMacros());
ASSERT_TRUE(System::TestTools::IsNull(doc->get_VbaProject()));
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
