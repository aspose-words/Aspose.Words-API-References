---
title: Aspose::Words::MailMerging::IMailMergeCallback interface
linktitle: IMailMergeCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::IMailMergeCallback interface. Implement this interface if you want to receive notifications while mail merge is performed in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface


Implement this interface if you want to receive notifications while mail merge is performed.

```cpp
class IMailMergeCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [TagsReplaced](./tagsreplaced/)() | Called when "mustache" text tags are replaced with MERGEFIELD fields. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
