---
title: "Aspose::Words::MailMerging::MappedDataFieldCollection 类"
linktitle: "MappedDataFieldCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::MappedDataFieldCollection 类。允许在数据源中的字段名称和文档中的邮件合并字段名称之间自动映射。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class


允许在数据源字段名称与文档中邮件合并字段名称之间自动映射。欲了解更多，请访问 [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) 文档文章。

```cpp
class MappedDataFieldCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | 添加新的字段映射。 |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | 从集合中移除所有元素。 |
| [ContainsKey](./containskey/)(const System::String\&) | 确定文档中指定字段的映射是否存在于集合中。 |
| [ContainsValue](./containsvalue/)(const System::String\&) | 确定数据源中指定字段的映射是否存在于集合中。 |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | 获取集合中包含的元素数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个字典枚举器对象，可用于遍历集合中的所有项。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | 获取或设置与指定邮件合并字段关联的数据源字段的名称。 |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | 获取或设置与指定邮件合并字段关联的数据源字段的名称。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | 移除字段映射。 |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| 类型定义 | 描述 |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## 备注


这实现为字符串键到字符串值的集合。键是文档中邮件合并字段的名称，值是数据源中字段的名称。

## 另见

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
