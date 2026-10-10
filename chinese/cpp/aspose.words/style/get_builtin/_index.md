---
title: "Aspose::Words::Style::get_BuiltIn 方法"
linktitle: "get_BuiltIn"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Style::get_BuiltIn 方法。如果此样式是 MS Word 中的内置样式之一，则为 true（在 C++ 中）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/style/get_builtin/
---
## Style::get_BuiltIn method


如果此样式是 MS Word 中的内置样式之一，则为 True。

```cpp
bool Aspose::Words::Style::get_BuiltIn()
```


## 示例



展示如何将自定义样式与内置样式区分开来。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 当我们使用 Microsoft Word 或通过 Aspose.Words 以编程方式创建文档时，
// 文档将附带一组样式，可应用于其文本以修改外观。
// 我们可以通过文档的 "Styles" 集合访问这些内置样式。
// 这些样式的 "BuiltIn" 标志全部设置为 "true"。
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"Emphasis");

ASSERT_TRUE(style->get_BuiltIn());

// 创建自定义样式并将其添加到集合中。
// 此类自定义样式的 "BuiltIn" 标志将设置为 "false"。
style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
style->get_Font()->set_Name(u"Courier New");

ASSERT_FALSE(style->get_BuiltIn());
```

## 另见

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
