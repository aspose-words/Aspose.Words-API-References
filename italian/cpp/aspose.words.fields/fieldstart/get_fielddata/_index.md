---
title: "Aspose::Words::Fields::FieldStart::get_FieldData metodo"
linktitle: "get_FieldData"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldStart::get_FieldData metodo. Ottiene i dati personalizzati del campo associati al campo in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.fields/fieldstart/get_fielddata/
---
## FieldStart::get_FieldData method


Ottiene i dati del campo personalizzato associati al campo.

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::Fields::FieldStart::get_FieldData() const
```


## Esempi



Mostra come ottenere i dati associati al campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - Field with data.docx");

System::SharedPtr<Aspose::Words::Fields::Field> field = doc->get_Range()->get_Fields()->idx_get(2);
std::cout << System::Text::Encoding::get_Default()->GetString(field->get_Start()->get_FieldData()) << std::endl;
```

## Vedi anche

* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
