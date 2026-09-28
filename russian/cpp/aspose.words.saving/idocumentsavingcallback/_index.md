---
title: "интерфейс Aspose::Words::Saving::IDocumentSavingCallback"
linktitle: "IDocumentSavingCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Интерфейс Aspose::Words::Saving::IDocumentSavingCallback. Реализуйте этот интерфейс, если хотите иметь собственный пользовательский метод, вызываемый во время сохранения документа на C++."
type: docs
weight: 41000
url: /ru/cpp/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface


Реализуйте этот интерфейс, если вы хотите иметь собственный пользовательский метод, вызываемый во время сохранения документа.

```cpp
class IDocumentSavingCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\>) | Это вызывается для уведомления о прогрессе сохранения документа. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
