---
title: GetFieldNames
second_title: Aspose.Words for C++ API Reference
description: Returns a collection of mail merge field names used by the field.
type: docs
weight: 79
url: /cpp/aspose.words.fields/fieldaddressblock/getfieldnames/
---
## FieldAddressBlock::GetFieldNames method


Returns a collection of mail merge field names used by the field.

```cpp
System::ArrayPtr<System::String> Aspose::Words::Fields::FieldAddressBlock::GetFieldNames() override
```


## Examples



Shows how to get mail merge field names used by a field. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Field sample - ADDRESSBLOCK.docx");

ArrayPtr<String> addressFieldsExpect = MakeArray<String>(
    {u"Company", u"First Name", u"Middle Name", u"Last Name", u"Suffix", u"Address 1", u"City", u"State", u"Country or Region", u"Postal Code"});

auto addressBlockField = System::DynamicCast<FieldAddressBlock>(doc->get_Range()->get_Fields()->idx_get(0));
ArrayPtr<String> addressBlockFieldNames = addressBlockField->GetFieldNames();
```

## See Also

* Class [FieldAddressBlock](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
