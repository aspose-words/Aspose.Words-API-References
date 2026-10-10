---
title: "Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions 构造函数"
linktitle: "FindReplaceOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions 构造函数。在 C++ 中使用默认设置初始化 FindReplaceOptions 类的新实例。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions::FindReplaceOptions() constructor


使用默认设置初始化 [FindReplaceOptions](../) 类的新实例。

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions()
```


## 示例



展示如何在替换模式中识别并使用替代项。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Jason gave money to Paul.");

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) gave money to ([A-z]+)");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_UseSubstitutions(true);

// 使用传统模式不支持许多高级功能，因此我们需要将其设置为 'false'。
options->set_LegacyMode(false);

doc->get_Range()->Replace(regex, u"$2 took money from $1", options);

ASSERT_EQ(doc->GetText(), u"Paul took money from Jason.\f");
```

## 另见

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection) constructor


使用指定方向初始化 [FindReplaceOptions](../) 类的新实例。

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 方向 | Aspose::Words::Replacing::FindReplaceDirection | 查找和替换操作的方向。 |

## 另见

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


使用指定的方向和替换回调初始化 [FindReplaceOptions](../) 类的新实例。

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(Aspose::Words::Replacing::FindReplaceDirection direction, const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 方向 | Aspose::Words::Replacing::FindReplaceDirection | 查找和替换操作的方向。 |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | 用于替换找到的文本的回调。 |

## 另见

* Enum [FindReplaceDirection](../../findreplacedirection/)
* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
## FindReplaceOptions::FindReplaceOptions(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) constructor


使用指定的替换回调初始化 [FindReplaceOptions](../) 类的新实例。

```cpp
Aspose::Words::Replacing::FindReplaceOptions::FindReplaceOptions(const System::SharedPtr<Aspose::Words::Replacing::IReplacingCallback> &replacingCallback)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| replacingCallback | const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\& | 用于替换找到的文本的回调。 |

## 另见

* Interface [IReplacingCallback](../../ireplacingcallback/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
