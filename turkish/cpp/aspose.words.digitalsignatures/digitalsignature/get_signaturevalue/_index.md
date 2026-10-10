---
title: "Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue metodu"
linktitle: "get_SignatureValue"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue metodu. C++'da bir imza değerini temsil eden bayt dizisini alır."
type: docs
weight: 6500
url: /tr/cpp/aspose.words.digitalsignatures/digitalsignature/get_signaturevalue/
---
## DigitalSignature::get_SignatureValue method


İmza değerini temsil eden bir bayt dizisini alır.

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue() const
```


## Örnekler



Dijital olarak imzalanmış bir belgeden dijital imza değerinin nasıl alınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Digitally signed.docx");

for (auto&& digitalSignature : doc->get_DigitalSignatures())
{
    System::String signatureValue = System::Convert::ToBase64String(digitalSignature->get_SignatureValue());
    ASSERT_EQ(System::String(u"K1cVLLg2kbJRAzT5WK+m++G8eEO+l7S+5ENdjMxxTXkFzGUfvwxREuJdSFj9AbD") + u"MhnGvDURv9KEhC25DDF1al8NRVR71TF3CjHVZXpYu7edQS5/yLw/k5CiFZzCp1+MmhOdYPcVO+Fm" + u"+9fKr2iNLeyYB+fgEeZHfTqTFM2WwAqo=", signatureValue);
}
```

## Ayrıca Bakınız

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
