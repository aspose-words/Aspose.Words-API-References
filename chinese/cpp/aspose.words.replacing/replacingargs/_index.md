---
title: "Aspose::Words::Replacing::ReplacingArgs 类"
linktitle: "ReplacingArgs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::ReplacingArgs 类。提供自定义替换操作的数据。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class


提供自定义替换操作的数据。欲了解更多，请访问[查找和替换](https://docs.aspose.com/words/cpp/find-and-replace/)文档文章。

```cpp
class ReplacingArgs : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_GroupIndex](./get_groupindex/)() const | 通过索引标识 [Match](./get_match/) 中要用 [Replacement](./get_replacement/) 字符串替换的捕获组。 |
| [get_GroupName](./get_groupname/)() const | 通过名称标识 [Match](./get_match/) 中要用 [Replacement](./get_replacement/) 字符串替换的捕获组。 |
| [get_Match](./get_match/)() const | 在 **Replace** 期间单次正则表达式匹配产生的 **Match**。 |
| [get_MatchEndNode](./get_matchendnode/)() const | 获取包含匹配结束位置的节点。 |
| [get_MatchNode](./get_matchnode/)() const | 获取包含匹配开始位置的节点。 |
| [get_MatchOffset](./get_matchoffset/)() const | 获取匹配的零基起始位置（相对于包含匹配开始位置的节点的起始处）。 |
| [get_Replacement](./get_replacement/)() const | 获取替换字符串。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GroupIndex](./set_groupindex/)(int32_t) | 用于 [Aspose::Words::Replacing::ReplacingArgs::get_GroupIndex](./get_groupindex/) 的设置器。 |
| [set_GroupName](./set_groupname/)(const System::String\&) | 用于 [Aspose::Words::Replacing::ReplacingArgs::get_GroupName](./get_groupname/) 的设置器。 |
| [set_Replacement](./set_replacement/)(const System::String\&) | 设置替换字符串。 |
| static [Type](./type/)() |  |

## 另见

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
