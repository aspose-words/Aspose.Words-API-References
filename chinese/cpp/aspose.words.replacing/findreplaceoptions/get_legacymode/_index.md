---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode 方法"
linktitle: "get_LegacyMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode 方法。 在 C++ 中，获取或设置一个布尔值，指示是否使用旧的查找/替换算法。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/get_legacymode/
---
## FindReplaceOptions::get_LegacyMode method


获取或设置一个布尔值，指示使用旧的查找/替换算法。

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode() const
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
