---
title: "Aspose::Words::Fields::FieldStart::get_FieldData método"
linktitle: "get_FieldData"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldStart::get_FieldData método. Obtiene datos de campo personalizados que están asociados al campo en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.fields/fieldstart/get_fielddata/
---
## FieldStart::get_FieldData method


Obtiene los datos personalizados del campo que están asociados con el campo.

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::Fields::FieldStart::get_FieldData() const
```


## Ejemplos



Muestra cómo obtener datos asociados al campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - Field with data.docx");

System::SharedPtr<Aspose::Words::Fields::Field> field = doc->get_Range()->get_Fields()->idx_get(2);
std::cout << System::Text::Encoding::get_Default()->GetString(field->get_Start()->get_FieldData()) << std::endl;
```

## Ver también

* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
