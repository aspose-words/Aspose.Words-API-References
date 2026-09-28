---
title: "Метод Aspose::Words::Loading::IDocumentLoadingCallback::Notify"
linktitle: "Уведомление"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Loading::IDocumentLoadingCallback::Notify. Вызывается для уведомления о прогрессе загрузки документа в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback::Notify method


Это вызывается для уведомления о прогрессе загрузки документа.

```cpp
virtual void Aspose::Words::Loading::IDocumentLoadingCallback::Notify(System::SharedPtr<Aspose::Words::Loading::DocumentLoadingArgs> args)=0
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| аргументы | System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\> | Аргумент события. |
## Примечания


Основное назначение этого интерфейса — позволить коду приложения получать статус прогресса и прерывать процесс загрузки.

Исключение должно быть выброшено из обратного вызова прогресса для прерывания, и его следует перехватить в коде потребителя.

## См. также

* Class [DocumentLoadingArgs](../../documentloadingargs/)
* Interface [IDocumentLoadingCallback](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
