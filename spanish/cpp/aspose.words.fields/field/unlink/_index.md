---
title: "Método Aspose::Words::Fields::Field::Unlink"
linktitle: "Desvincular"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::Field::Unlink. Realiza la desvinculación del campo en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words.fields/field/unlink/
---
## Field::Unlink method


Ejecuta la desvinculación del campo.

```cpp
bool Aspose::Words::Fields::Field::Unlink()
```


### ReturnValue

**true** if the field has been unlinked, otherwise **false**.
## Observaciones


Reemplaza el campo con su resultado más reciente.

Algunos campos, como los campos XE (Entrada de índice) y los campos SEQ (Secuencia), no pueden desvincularse.

## Ejemplos



Muestra cómo desvincular un campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");
doc->get_Range()->get_Fields()->idx_get(1)->Unlink();
```

## Ver también

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
