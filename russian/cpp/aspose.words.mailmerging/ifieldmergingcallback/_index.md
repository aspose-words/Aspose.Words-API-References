---
title: "Aspose::Words::MailMerging::IFieldMergingCallback интерфейс"
linktitle: "IFieldMergingCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Интерфейс Aspose::Words::MailMerging::IFieldMergingCallback. Реализуйте этот интерфейс, если вы хотите контролировать, как данные вставляются в поля слияния во время операции слияния почты в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.mailmerging/ifieldmergingcallback/
---
## IFieldMergingCallback interface


Реализуйте этот интерфейс, если хотите контролировать, как данные вставляются в поля слияния во время операции слияния почты.

```cpp
class IFieldMergingCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [FieldMerging](./fieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::FieldMergingArgs\>) | Вызывается, когда движок слияния почты Aspose.Words собирается вставить данные в поле слияния в документе. |
| [GetType](./gettype/)() const override |  |
| virtual [ImageFieldMerging](./imagefieldmerging/)(System::SharedPtr\<Aspose::Words::MailMerging::ImageFieldMergingArgs\>) | Вызывается, когда движок слияния почты Aspose.Words собирается вставить изображение в поле слияния. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
