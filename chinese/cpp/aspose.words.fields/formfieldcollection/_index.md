---
title: "Aspose::Words::Fields::FormFieldCollection 类"
linktitle: "FormFieldCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FormFieldCollection 类。一个 FormField 对象的集合，表示范围内的所有表单字段。了解更多，请访问 C++ 文档文章。"
type: docs
weight: 113000
url: /zh/cpp/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class


一个 [FormField](../formfield/) 对象的集合，表示范围内的所有表单字段。了解更多，请访问 [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/) 文档文章。

```cpp
class FormFieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::FormField>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clear](./clear/)() | 从此集合和文档中移除所有表单字段。 |
| [get_Count](./get_count/)() | 返回集合中表单字段的数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 返回指定索引处的表单字段。 |
| [idx_get](./idx_get/)(const System::String\&) | 通过书签名称返回表单字段。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | 移除具有指定名称的表单字段。 |
| [RemoveAt](./removeat/)(int32_t) | 移除指定索引处的表单字段。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
