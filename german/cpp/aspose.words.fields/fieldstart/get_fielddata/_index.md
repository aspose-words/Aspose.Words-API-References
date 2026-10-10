---
title: "Methode Aspose::Words::Fields::FieldStart::get_FieldData"
linktitle: "get_FieldData"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Methode Aspose::Words::Fields::FieldStart::get_FieldData. Ruft benutzerdefinierte Felddaten ab, die mit dem Feld in C++ verknüpft sind."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldstart/get_fielddata/
---
## FieldStart::get_FieldData method


Ruft benutzerdefinierte Felddaten ab, die dem Feld zugeordnet sind.

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::Fields::FieldStart::get_FieldData() const
```


## Beispiele



Zeigt, wie man Daten abruft, die mit dem Feld verknüpft sind.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - Field with data.docx");

System::SharedPtr<Aspose::Words::Fields::Field> field = doc->get_Range()->get_Fields()->idx_get(2);
std::cout << System::Text::Encoding::get_Default()->GetString(field->get_Start()->get_FieldData()) << std::endl;
```

## Siehe auch

* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
