---
title: "Aspose::Words::MailMerging::IMailMergeDataSource interface"
linktitle: "IMailMergeDataSource"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::IMailMergeDataSource 接口。实现此接口以允许从自定义数据源（例如对象列表）进行邮件合并。C++ 还支持主从数据。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface


实现此接口以允许从自定义数据源（例如对象列表）进行邮件合并。还支持主从数据。

```cpp
class IMailMergeDataSource : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [get_TableName](./get_tablename/)() | 返回数据源的名称。 |
| virtual [GetChildDataSource](./getchilddatasource/)(System::String) | Aspose.Words 邮件合并引擎在遇到嵌套邮件合并区域的开始时调用此方法。 |
| [GetType](./gettype/)() const override |  |
| virtual [GetValue](./getvalue/)(System::String, System::SharedPtr\<System::Object\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [MoveNext](./movenext/)() | 将数据源移动到下一条记录。 |
| static [Type](./type/)() |  |
## 备注


创建数据源时，应将其初始化为指向 BOF（第一条记录之前）。Aspose.Words 邮件合并引擎将调用 [MoveNext](./movenext/) 以移动到下一条记录，然后调用 [GetValue()](./getvalue/) 来获取文档或当前邮件合并区域中遇到的每个合并字段的值。

## 另见

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
