---
title: "Aspose::Words::Saving::IDocumentPartSavingCallback interface"
linktitle: "IDocumentPartSavingCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::IDocumentPartSavingCallback interface. Реализуйте этот интерфейс, если вы хотите получать уведомления и контролировать, как Aspose.Words сохраняет части документа при экспорте документа в формат Html или Epub на C++."
type: docs
weight: 40000
url: /ru/cpp/aspose.words.saving/idocumentpartsavingcallback/
---
## IDocumentPartSavingCallback interface


Реализуйте этот интерфейс, если вы хотите получать уведомления и контролировать, как Aspose.Words сохраняет части документа при экспорте документа в формат [Html](../../aspose.words/saveformat/) или [Epub](../../aspose.words/saveformat/).

```cpp
class IDocumentPartSavingCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [DocumentPartSaving](./documentpartsaving/)(System::SharedPtr\<Aspose::Words::Saving::DocumentPartSavingArgs\>) | Вызывается, когда Aspose.Words собирается сохранить часть документа. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
