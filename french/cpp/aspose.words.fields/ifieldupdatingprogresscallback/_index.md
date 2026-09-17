---
title: "Aspose::Words::Fields::IFieldUpdatingProgressCallback interface"
linktitle: "IFieldUpdatingProgressCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::IFieldUpdatingProgressCallback interface. Implémentez cette interface si vous souhaitez suivre la progression de la mise à jour des champs en C++."
type: docs
weight: 124000
url: /fr/cpp/aspose.words.fields/ifieldupdatingprogresscallback/
---
## IFieldUpdatingProgressCallback interface


Implémentez cette interface si vous souhaitez suivre la progression de la mise à jour du champ.

```cpp
class IFieldUpdatingProgressCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Fields::FieldUpdatingProgressArgs\>) | Une méthode définie par l'utilisateur qui est appelée lorsque la progression de la mise à jour change. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
