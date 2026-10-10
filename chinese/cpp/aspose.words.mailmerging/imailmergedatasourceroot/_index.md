---
title: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot interface"
linktitle: "IMailMergeDataSourceRoot"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot interface. 实现此接口，以便在 C++ 中使用自定义主从数据源进行邮件合并。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.mailmerging/imailmergedatasourceroot/
---
## IMailMergeDataSourceRoot interface


实现此接口以允许从具有主从数据的自定义数据源进行邮件合并。

```cpp
class IMailMergeDataSourceRoot : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [GetDataSource](./getdatasource/)(System::String) | Aspose.Words 邮件合并引擎在遇到顶级邮件合并区域的开始时调用此方法。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
