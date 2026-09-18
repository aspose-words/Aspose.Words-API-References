---
title: "Aspose::Words::Fields::FormFieldCollection Klasse"
linktitle: "FormFieldCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FormFieldCollection Klasse. Eine Sammlung von FormField-Objekten, die alle Formularfelder in einem Bereich darstellen. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 113000
url: /de/cpp/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class


Eine Sammlung von [FormField](../formfield/)-Objekten, die alle Formularfelder in einem Bereich darstellen. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/).

```cpp
class FormFieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::FormField>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clear](./clear/)() | Entfernt alle Formularfelder aus dieser Sammlung und aus dem Dokument. |
| [get_Count](./get_count/)() | Gibt die Anzahl der Formularfelder in der Sammlung zurück. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator-Objekt zurück. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gibt ein Formularfeld am angegebenen Index zurück. |
| [idx_get](./idx_get/)(const System::String\&) | Gibt ein Formularfeld anhand des Lesezeichennamens zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Entfernt ein Formularfeld mit dem angegebenen Namen. |
| [RemoveAt](./removeat/)(int32_t) | Entfernt ein Formularfeld am angegebenen Index. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
