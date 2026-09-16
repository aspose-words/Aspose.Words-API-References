---
title: "Aspose::Words::MailMerging::IMailMergeCallback interface"
linktitle: "IMailMergeCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::IMailMergeCallback 接口。如果您希望在 C++ 中执行邮件合并时接收通知，请实现此接口。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface


如果您希望在执行邮件合并时接收通知，请实现此接口。

```cpp
class IMailMergeCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [TagsReplaced](./tagsreplaced/)() | 当 "mustache" 文本标签被替换为 MERGEFIELD 字段时调用。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
