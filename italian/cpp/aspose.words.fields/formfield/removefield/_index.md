---
title: "Aspose::Words::Fields::FormField::RemoveField metodo"
linktitle: "RemoveField"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FormField::RemoveField metodo. Rimuove l'intero campo modulo, non solo il carattere speciale del campo modulo in C++."
type: docs
weight: 27000
url: /it/cpp/aspose.words.fields/formfield/removefield/
---
## FormField::RemoveField method


Rimuove l'intero campo modulo, non solo il carattere speciale del campo modulo.

```cpp
void Aspose::Words::Fields::FormField::RemoveField()
```


## Esempi



Mostra come eliminare un campo modulo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(3);
formField->RemoveField();
```

## Vedi anche

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
