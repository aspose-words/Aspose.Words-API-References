---
title: "Aspose::Words::Fields::FormFieldCollection classe"
linktitle: "FormFieldCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FormFieldCollection classe. Una raccolta di oggetti FormField che rappresentano tutti i campi modulo in un intervallo. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 113000
url: /it/cpp/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class


Una raccolta di oggetti [FormField](../formfield/) che rappresentano tutti i campi modulo in un intervallo. Per saperne di più, visita l'articolo di documentazione [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/).

```cpp
class FormFieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::FormField>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clear](./clear/)() | Rimuove tutti i campi modulo da questa raccolta e dal documento. |
| [get_Count](./get_count/)() | Restituisce il numero di campi modulo nella raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Restituisce un campo modulo all'indice specificato. |
| [idx_get](./idx_get/)(const System::String\&) | Restituisce un campo modulo per nome segnalibro. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Rimuove un campo modulo con il nome specificato. |
| [RemoveAt](./removeat/)(int32_t) | Rimuove un campo modulo all'indice specificato. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
