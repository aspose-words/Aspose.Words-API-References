---
title: "Aspose::Words::Fields::FormField::RemoveField‑Methode"
linktitle: "RemoveField"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FormField::RemoveField‑Methode. Entfernt das gesamte Formularfeld, nicht nur das spezielle Formularfeldzeichen in C++."
type: docs
weight: 27000
url: /de/cpp/aspose.words.fields/formfield/removefield/
---
## FormField::RemoveField method


Entfernt das komplette Formularfeld, nicht nur das Sonderzeichen des Formularfelds.

```cpp
void Aspose::Words::Fields::FormField::RemoveField()
```


## Beispiele



Zeigt, wie ein Formularfeld gelöscht wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(3);
formField->RemoveField();
```

## Siehe auch

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
