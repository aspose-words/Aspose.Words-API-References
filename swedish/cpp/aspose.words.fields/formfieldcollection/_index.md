---
title: "Aspose::Words::Fields::FormFieldCollection klass"
linktitle: "FormFieldCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FormFieldCollection klass. En samling av FormField-objekt som representerar alla formulärfält i ett område. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 113000
url: /sv/cpp/aspose.words.fields/formfieldcollection/
---
## FormFieldCollection class


En samling av [FormField](../formfield/) objekt som representerar alla formulärfält i ett område. För att lära dig mer, besök dokumentationsartikeln [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/).

```cpp
class FormFieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::FormField>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clear](./clear/)() | Tar bort alla formulärfält från denna samling och från dokumentet. |
| [get_Count](./get_count/)() | Returnerar antalet formulärfält i samlingen. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returnerar ett formulärfält på det angivna indexet. |
| [idx_get](./idx_get/)(const System::String\&) | Returnerar ett formulärfält efter bokmärkesnamn. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Tar bort ett formulärfält med det angivna namnet. |
| [RemoveAt](./removeat/)(int32_t) | Tar bort ett formulärfält på det angivna indexet. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
