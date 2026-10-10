---
title: "Interface Aspose::Words::IRevisionCriteria"
linktitle: "IRevisionCriteria"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Interface Aspose::Words::IRevisionCriteria. Implémentez cette interface si vous souhaitez contrôler quand une certaine Révision doit être acceptée/rejetée ou non par les méthodes Accept()/Reject() en C++."
type: docs
weight: 79500
url: /fr/cpp/aspose.words/irevisioncriteria/
---
## IRevisionCriteria interface


Implémentez cette interface si vous souhaitez contrôler quand une certaine [Revision](../revision/) doit être acceptée/rejetée ou non par les méthodes [Accept()](../)/[Reject()](../).

```cpp
class IRevisionCriteria : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [IsMatch](./ismatch/)(System::SharedPtr\<Aspose::Words::Revision\>) | Vérifie si la *revision* spécifiée correspond aux critères ou non. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
