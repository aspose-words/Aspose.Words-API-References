---
title: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId 方法"
linktitle: "get_IgnoreStoreItemId"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId 方法。指定是否在 C++ 中忽略 StructuredDocumentTag 存储项 Id 的差异。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.comparing/advancedcompareoptions/get_ignorestoreitemid/
---
## AdvancedCompareOptions::get_IgnoreStoreItemId method


指定是否忽略 StructuredDocumentTag 存储项标识的差异。

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId() const
```


## 示例



展示如何比较内容相同但存储项标识不同的 SDT。
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// 配置选项以比较内容相同但存储项标识不同的 SDT。
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## 另见

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
