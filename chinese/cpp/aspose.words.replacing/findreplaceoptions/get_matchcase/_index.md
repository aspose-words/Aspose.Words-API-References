---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase 方法"
linktitle: "get_MatchCase"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase 方法。 在 C++ 中，True 表示区分大小写比较，false 表示不区分大小写比较。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/get_matchcase/
---
## FindReplaceOptions::get_MatchCase method


True 表示区分大小写比较，false 表示不区分大小写比较。

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase() const
```


## 示例



展示如何在执行查找替换操作时切换大小写敏感性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// 我们可以使用 "FindReplaceOptions" 对象来修改查找替换过程。
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// 将 "MatchCase" 标志设置为 "true"，以在查找要替换的字符串时启用大小写敏感。
// 将 "MatchCase" 标志设置为 "false"，以在搜索要替换的文本时忽略字符大小写。
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```

## 另见

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
