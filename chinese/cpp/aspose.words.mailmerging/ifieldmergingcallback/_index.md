---
title: "Aspose::Words::MailMerging::IFieldMergingCallback interface"
linktitle: "IFieldMergingCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::IFieldMergingCallback 接口。如果您想在 C++ 中控制邮件合并操作期间数据如何插入合并字段，请实现此接口。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.mailmerging/ifieldmergingcallback/
---
## IFieldMergingCallback interface


如果您希望控制在邮件合并操作期间数据如何插入合并字段，请实现此接口。

```cpp
class IFieldMergingCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [FieldMerging](./fieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::FieldMergingArgs\>) | 当 Aspose.Words 邮件合并引擎即将在文档中的合并字段插入数据时调用。 |
| [GetType](./gettype/)() const override |  |
| virtual [ImageFieldMerging](./imagefieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::ImageFieldMergingArgs\>) | 当 Aspose.Words 邮件合并引擎即将在合并字段中插入图像时调用。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
