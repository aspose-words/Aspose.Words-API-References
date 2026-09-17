---
title: "Aspose::Words::Fields::FormFieldCollection classe"
linktitle: "FormFieldCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FormFieldCollection classe. Une collection d'objets FormField qui représentent tous les champs de formulaire dans une plage. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 113000
url: /fr/cpp/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class


Une collection d'objets [FormField](../formfield/) qui représentent tous les champs de formulaire dans une plage. Pour en savoir plus, consultez l'article de documentation [Travailler avec les champs de formulaire](https://docs.aspose.com/words/cpp/working-with-form-fields/).

```cpp
class FormFieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::FormField>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clear](./clear/)() | Supprime tous les champs de formulaire de cette collection et du document. |
| [get_Count](./get_count/)() | Renvoie le nombre de champs de formulaire dans la collection. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Renvoie un champ de formulaire à l'index spécifié. |
| [idx_get](./idx_get/)(const System::String\&) | Renvoie un champ de formulaire par le nom du signet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Supprime un champ de formulaire avec le nom spécifié. |
| [RemoveAt](./removeat/)(int32_t) | Supprime un champ de formulaire à l'index spécifié. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
