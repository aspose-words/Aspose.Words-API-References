---
title: "Aspose::Words::Fields::FieldStart::get_FieldData-metoden"
linktitle: "get_FieldData"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldStart::get_FieldData-metoden. Hämtar anpassad fältdata som är associerad med fältet i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.fields/fieldstart/get_fielddata/
---
## FieldStart::get_FieldData method


Hämtar anpassade fältdata som är associerade med fältet.

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::Fields::FieldStart::get_FieldData() const
```


## Exempel



Visar hur man hämtar data som är associerad med fältet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - Field with data.docx");

System::SharedPtr<Aspose::Words::Fields::Field> field = doc->get_Range()->get_Fields()->idx_get(2);
std::cout << System::Text::Encoding::get_Default()->GetString(field->get_Start()->get_FieldData()) << std::endl;
```

## Se även

* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
