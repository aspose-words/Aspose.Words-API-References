---
title: Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue method
linktitle: get_SignatureValue
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue method. Gets an array of bytes representing a signature value in C++.'
type: docs
weight: 6500
url: /cpp/aspose.words.digitalsignatures/digitalsignature/get_signaturevalue/
---
## DigitalSignature::get_SignatureValue method


Gets an array of bytes representing a signature value.

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue() const
```


## Examples



Shows how to get a digital signature value from a digitally signed document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Digitally signed.docx");

for (auto&& digitalSignature : doc->get_DigitalSignatures())
{
    System::String signatureValue = System::Convert::ToBase64String(digitalSignature->get_SignatureValue());
    ASSERT_EQ(System::String(u"K1cVLLg2kbJRAzT5WK+m++G8eEO+l7S+5ENdjMxxTXkFzGUfvwxREuJdSFj9AbD") + u"MhnGvDURv9KEhC25DDF1al8NRVR71TF3CjHVZXpYu7edQS5/yLw/k5CiFZzCp1+MmhOdYPcVO+Fm" + u"+9fKr2iNLeyYB+fgEeZHfTqTFM2WwAqo=", signatureValue);
}
```

## See Also

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
