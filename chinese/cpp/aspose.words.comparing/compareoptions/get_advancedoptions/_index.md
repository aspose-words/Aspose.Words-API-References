---
title: "Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions 方法"
linktitle: "get_AdvancedOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions 方法。指定可能有助于在 C++ 中生成更精确比较输出的高级比较选项。"
type: docs
weight: 2500
url: /zh/cpp/aspose.words.comparing/compareoptions/get_advancedoptions/
---
## CompareOptions::get_AdvancedOptions method


指定高级比较选项，可能有助于生成更精确的比较输出。

```cpp
const System::SharedPtr<Aspose::Words::Comparing::AdvancedCompareOptions> & Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions() const
```


## 示例



展示如何在忽略 DML 唯一 ID 的情况下比较文档。
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID original.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID compare.docx");

// 默认情况下，Aspose.Words 不会忽略 DML 的唯一 ID，修订计数为 2。
// 如果我们忽略 DML 的唯一 ID，修订计数将为 0。
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreDmlUniqueId(isIgnoreDmlUniqueId);

docA->Compare(docB, u"Aspose.Words", System::DateTime::get_Now(), compareOptions);

ASSERT_EQ(isIgnoreDmlUniqueId ? 0 : 2, docA->get_Revisions()->get_Count());
```

## 另见

* Class [AdvancedCompareOptions](../../advancedcompareoptions/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
