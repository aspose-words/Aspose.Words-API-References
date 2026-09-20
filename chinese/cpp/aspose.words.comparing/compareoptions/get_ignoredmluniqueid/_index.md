---
title: "Aspose::Words::Comparing::CompareOptions::get_IgnoreDmlUniqueId 方法"
linktitle: "get_IgnoreDmlUniqueId"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comparing::CompareOptions::get_IgnoreDmlUniqueId 方法。指定是否在 C++ 中忽略 DrawingML 唯一标识的差异。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.comparing/compareoptions/get_ignoredmluniqueid/
---
## CompareOptions::get_IgnoreDmlUniqueId method


指定是否忽略 DrawingML 唯一标识的差异。

```cpp
bool Aspose::Words::Comparing::CompareOptions::get_IgnoreDmlUniqueId()
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

* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
