---
title: "Aspose::Words::MailMerging::IMailMergeCallback interface"
linktitle: "IMailMergeCallback"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::MailMerging::IMailMergeCallback. نفّذ هذه الواجهة إذا كنت تريد تلقي الإشعارات أثناء تنفيذ دمج البريد في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface


نفّذ هذه الواجهة إذا كنت تريد تلقي الإشعارات أثناء تنفيذ دمج البريد.

```cpp
class IMailMergeCallback : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [TagsReplaced](./tagsreplaced/)() | يتم استدعاؤها عندما يتم استبدال وسوم النص "mustache" بحقول MERGEFIELD. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
