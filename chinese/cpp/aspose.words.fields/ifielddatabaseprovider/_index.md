---
title: "Aspose::Words::Fields::IFieldDatabaseProvider 接口"
linktitle: "IFieldDatabaseProvider"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::IFieldDatabaseProvider 接口。实现此接口以在 C++ 中更新 FieldDatabase 字段时提供数据。"
type: docs
weight: 120000
url: /zh/cpp/aspose.words.fields/ifielddatabaseprovider/
---
## IFieldDatabaseProvider interface


实现此接口以在更新时为 [FieldDatabase](../fielddatabase/) 字段提供数据。

```cpp
class IFieldDatabaseProvider : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [GetQueryResult](./getqueryresult/)(System::String, System::String, System::String, System::SharedPtr\<Aspose::Words::Fields::FieldDatabase\>) | 返回查询结果。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
