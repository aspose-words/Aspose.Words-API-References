---
title: "Aspose::Words::MailMerging::IMailMergeCallback interface"
linktitle: "IMailMergeCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::MailMerging::IMailMergeCallback interface. Реализуйте этот интерфейс, если хотите получать уведомления во время выполнения слияния почты в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface


Реализуйте этот интерфейс, если хотите получать уведомления во время выполнения слияния почты.

```cpp
class IMailMergeCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [TagsReplaced](./tagsreplaced/)() | Вызывается, когда текстовые теги "mustache" заменяются полями MERGEFIELD. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
