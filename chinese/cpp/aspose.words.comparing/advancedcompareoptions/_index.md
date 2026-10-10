---
title: "Aspose::Words::Comparing::AdvancedCompareOptions 类"
linktitle: "AdvancedCompareOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comparing::AdvancedCompareOptions 类。允许在 C++ 中设置高级比较选项。"
type: docs
weight: 500
url: /zh/cpp/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class


允许设置高级比较选项。

```cpp
class AdvancedCompareOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [AdvancedCompareOptions](./advancedcompareoptions/)() |  |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() const | 指定是否忽略 DrawingML 唯一标识的差异。 |
| [get_IgnoreStoreItemId](./get_ignorestoreitemid/)() const | 指定是否忽略 StructuredDocumentTag 存储项标识的差异。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | 用于设置 [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/) 的 setter。 |
| [set_IgnoreStoreItemId](./set_ignorestoreitemid/)(bool) | 用于设置 [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId](./get_ignorestoreitemid/) 的 setter。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
