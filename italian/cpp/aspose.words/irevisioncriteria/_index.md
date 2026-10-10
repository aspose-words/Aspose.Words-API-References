---
title: "Aspose::Words::IRevisionCriteria interface"
linktitle: "IRevisionCriteria"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::IRevisionCriteria interface. Implementa questa interfaccia se desideri controllare quando una determinata Revision deve essere accettata/rifiutata o meno mediante i metodi Accept()/Reject() in C++."
type: docs
weight: 79500
url: /it/cpp/aspose.words/irevisioncriteria/
---
## IRevisionCriteria interface


Implementa questa interfaccia se desideri controllare quando una determinata [Revision](../revision/) deve essere accettata/rifiutata o meno mediante i metodi [Accept()](../)/[Reject()](../).

```cpp
class IRevisionCriteria : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [IsMatch](./ismatch/)(System::SharedPtr\<Aspose::Words::Revision\>) | Verifica se la *revision* specificata corrisponde o meno ai criteri. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
