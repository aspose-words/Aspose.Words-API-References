---
title: "Aspose::Words::Fields::FormField::RemoveField método"
linktitle: "RemoveField"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FormField::RemoveField método. Elimina el campo de formulario completo, no solo el carácter especial del campo de formulario en C++."
type: docs
weight: 27000
url: /es/cpp/aspose.words.fields/formfield/removefield/
---
## FormField::RemoveField method


Elimina el campo de formulario completo, no solo el carácter especial del campo de formulario.

```cpp
void Aspose::Words::Fields::FormField::RemoveField()
```


## Ejemplos



Muestra cómo eliminar un campo de formulario.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(3);
formField->RemoveField();
```

## Ver también

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
