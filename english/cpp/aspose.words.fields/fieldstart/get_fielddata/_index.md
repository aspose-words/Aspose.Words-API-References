---
title: Aspose::Words::Fields::FieldStart::get_FieldData method
linktitle: get_FieldData
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldStart::get_FieldData method. Gets custom field data which is associated with the field in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.fields/fieldstart/get_fielddata/
---
## FieldStart::get_FieldData method


Gets custom field data which is associated with the field.

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::Fields::FieldStart::get_FieldData() const
```


## Examples



Shows how to get data associated with the field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - Field with data.docx");

System::SharedPtr<Aspose::Words::Fields::Field> field = doc->get_Range()->get_Fields()->idx_get(2);
std::cout << System::Text::Encoding::get_Default()->GetString(field->get_Start()->get_FieldData()) << std::endl;
```

## See Also

* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
