---
title: "Aspose::Words::Fields::IFieldUpdateCultureProvider interface"
linktitle: "IFieldUpdateCultureProvider"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::IFieldUpdateCultureProvider interface. Lorsqu'elle est implémentée, fournit un objet CultureInfo qui doit être utilisé lors de la mise à jour d'un champ particulier en C++."
type: docs
weight: 122000
url: /fr/cpp/aspose.words.fields/ifieldupdatecultureprovider/
---
## IFieldUpdateCultureProvider interface


Lorsqu'elle est implémentée, elle fournit un objet **CultureInfo** qui doit être utilisé lors de la mise à jour d'un champ particulier.

```cpp
class IFieldUpdateCultureProvider : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [GetCulture](./getculture/)(System::String, System::SharedPtr\<Aspose::Words::Fields::Field\>) | Renvoie un objet **CultureInfo** à utiliser lors de la mise à jour du champ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
