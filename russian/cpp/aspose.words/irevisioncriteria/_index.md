---
title: "Интерфейс Aspose::Words::IRevisionCriteria"
linktitle: "IRevisionCriteria"
second_title: "Справочник API Aspose.Words для C++"
description: "Интерфейс Aspose::Words::IRevisionCriteria. Реализуйте этот интерфейс, если хотите контролировать, когда определённая Revision должна быть принята/отклонена методами Accept()/Reject() в C++."
type: docs
weight: 79500
url: /ru/cpp/aspose.words/irevisioncriteria/
---
## IRevisionCriteria interface


Реализуйте этот интерфейс, если хотите контролировать, когда определённый [Revision](../revision/) должен быть принят/отклонён методами [Accept()](../) и [Reject()](../).

```cpp
class IRevisionCriteria : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [IsMatch](./ismatch/)(System::SharedPtr\<Aspose::Words::Revision\>) | Проверяет, соответствует ли указанный *revision* критериям. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
