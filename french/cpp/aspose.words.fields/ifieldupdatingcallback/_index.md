---
title: "Aspose::Words::Fields::IFieldUpdatingCallback interface"
linktitle: "IFieldUpdatingCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::IFieldUpdatingCallback interface. Implémentez cette interface si vous souhaitez que vos propres méthodes personnalisées soient appelées lors d'une mise à jour de champ en C++."
type: docs
weight: 123000
url: /fr/cpp/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface


Implémentez cette interface si vous souhaitez que vos propres méthodes personnalisées soient appelées lors d'une mise à jour de champ.

```cpp
class IFieldUpdatingCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [FieldUpdated](./fieldupdated/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | Une méthode définie par l'utilisateur qui est appelée juste après la mise à jour d'un champ. |
| virtual [FieldUpdating](./fieldupdating/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | Une méthode définie par l'utilisateur qui est appelée juste avant la mise à jour d'un champ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
