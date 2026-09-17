---
title: "Interface Aspose::Words::Replacing::IReplacingCallback"
linktitle: "IReplacingCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Interface Aspose::Words::Replacing::IReplacingCallback. Implémentez cette interface si vous souhaitez disposer de votre propre méthode personnalisée appelée pendant une opération de recherche et de remplacement en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface


Implémentez cette interface si vous souhaitez disposer de votre propre méthode personnalisée appelée pendant une opération de recherche et de remplacement.

```cpp
class IReplacingCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Replacing](./replacing/)(System::SharedPtr\<Aspose::Words::Replacing::ReplacingArgs\>) | Une méthode définie par l'utilisateur qui est appelée pendant une opération de remplacement pour chaque correspondance trouvée juste avant qu'un remplacement ne soit effectué. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
