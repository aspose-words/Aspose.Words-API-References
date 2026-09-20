---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes method"
linktitle: "get_IgnoreFieldCodes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes method. 获取或设置一个布尔值，指示是否忽略字段代码内部的文本。默认值在 C++ 中为 false。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefieldcodes/
---
## FindReplaceOptions::get_IgnoreFieldCodes method


获取或设置一个布尔值，指示是否忽略字段代码中的文本。默认值为 **false**。

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes() const
```

## 备注


此选项仅影响字段代码（它不会忽略位于 [FieldSeparator](../../../aspose.words/nodetype/) 和 [FieldEnd](../../../aspose.words/nodetype/) 之间的节点）。

要忽略整个字段，请使用相应的选项 [IgnoreFields](../get_ignorefields/)。

## 示例



展示如何忽略字段代码内部的文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u"INCLUDETEXT", u"Test IT!");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFieldCodes(ignoreFieldCodes);

// 在文档中替换 'T'，是否忽略字段代码内部的文本。
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"T"), u"*", options);
std::cout << doc->GetText() << std::endl;

ASSERT_EQ(ignoreFieldCodes ? System::String(u"\u0013INCLUDETEXT\u0014*est I*!\u0015") : System::String(u"\u0013INCLUDE*EX*\u0014*est I*!\u0015"), doc->GetText().Trim());
```

## 另见

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
