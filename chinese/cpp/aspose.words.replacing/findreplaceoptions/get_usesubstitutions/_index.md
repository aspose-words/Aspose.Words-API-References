---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions 方法"
linktitle: "get_UseSubstitutions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions 方法。获取或设置一个布尔值，指示是否在替换模式中识别并使用替代项。默认值在 C++ 中为 false。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/get_usesubstitutions/
---
## FindReplaceOptions::get_UseSubstitutions method


获取或设置一个布尔值，指示是否在替换模式中识别并使用替代项。默认值为 **false**。

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions() const
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


展示如何使用替代项替换文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"John sold a car to Paul.");
builder->Writeln(u"Jane sold a house to Joe.");

// 我们可以使用 "FindReplaceOptions" 对象来修改查找替换过程。
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// 将 "UseSubstitutions" 属性设置为 "true" 以获取
// 查找和替换操作，以识别替代元素。
// 将 "UseSubstitutions" 属性设置为 "false" 以忽略替代元素。
options->set_UseSubstitutions(useSubstitutions);

auto regex = System::MakeObject<System::Text::RegularExpressions::Regex>(u"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc->get_Range()->Replace(regex, u"$3 bought a $2 from $1", options);

ASSERT_EQ(useSubstitutions ? System::String(u"Paul bought a car from John.\rJoe bought a house from Jane.") : System::String(u"$3 bought a $2 from $1.\r$3 bought a $2 from $1."), doc->GetText().Trim());
```

## 另见

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
