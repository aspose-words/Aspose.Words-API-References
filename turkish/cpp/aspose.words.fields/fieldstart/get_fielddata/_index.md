---
title: "Aspose::Words::Fields::FieldStart::get_FieldData yöntemi"
linktitle: "get_FieldData"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldStart::get_FieldData yöntemi. C++'ta alanla ilişkili özel alan verilerini alır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.fields/fieldstart/get_fielddata/
---
## FieldStart::get_FieldData method


Alanla ilişkili özel alan verilerini alır.

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::Fields::FieldStart::get_FieldData() const
```


## Örnekler



Alanla ilişkili verilerin nasıl alınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - Field with data.docx");

System::SharedPtr<Aspose::Words::Fields::Field> field = doc->get_Range()->get_Fields()->idx_get(2);
std::cout << System::Text::Encoding::get_Default()->GetString(field->get_Start()->get_FieldData()) << std::endl;
```

## Ayrıca Bakınız

* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
