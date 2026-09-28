---
title: "Метод Aspose::Words::Saving::IDocumentSavingCallback::Notify"
linktitle: "Уведомление"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::IDocumentSavingCallback::Notify. Вызывается для уведомления о прогрессе сохранения документа в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback::Notify method


Это вызывается для уведомления о прогрессе сохранения документа.

```cpp
virtual void Aspose::Words::Saving::IDocumentSavingCallback::Notify(System::SharedPtr<Aspose::Words::Saving::DocumentSavingArgs> args)=0
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| аргументы | System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\> | Аргумент события. |
## Примечания


Основное назначение этого интерфейса — позволить коду приложения получать статус прогресса и прерывать процесс сохранения.

Исключение должно быть выброшено из обратного вызова прогресса для прерывания, и его следует перехватить в коде потребителя.

## См. также

* Class [DocumentSavingArgs](../../documentsavingargs/)
* Interface [IDocumentSavingCallback](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
