---
title: "Aspose::Words::Fields::FormField::RemoveField metod"
linktitle: "RemoveField"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FormField::RemoveField metod. Tar bort hela formulärfältet, inte bara det speciella tecknet för formulärfältet i C++."
type: docs
weight: 27000
url: /sv/cpp/aspose.words.fields/formfield/removefield/
---
## FormField::RemoveField method


Tar bort hela formulärfältet, inte bara det speciella tecknet för formulärfältet.

```cpp
void Aspose::Words::Fields::FormField::RemoveField()
```


## Exempel



Visar hur man tar bort ett formulärfält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(3);
formField->RemoveField();
```

## Se även

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
