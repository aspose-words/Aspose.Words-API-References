---
title: "Интерфейс Aspose::Words::Loading::IDocumentLoadingCallback"
linktitle: "IDocumentLoadingCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Интерфейс Aspose::Words::Loading::IDocumentLoadingCallback. Реализуйте этот интерфейс, если хотите иметь собственный пользовательский метод, вызываемый при загрузке документа в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface


Реализуйте этот интерфейс, если вы хотите иметь собственный пользовательский метод, вызываемый во время загрузки документа.

```cpp
class IDocumentLoadingCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\>) | Это вызывается для уведомления о прогрессе загрузки документа. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
