---
title: "Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue metodo"
linktitle: "get_SignatureValue"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue metodo. Ottiene un array di byte che rappresenta il valore di una firma in C++."
type: docs
weight: 6500
url: /it/cpp/aspose.words.digitalsignatures/digitalsignature/get_signaturevalue/
---
## DigitalSignature::get_SignatureValue method


Ottiene un array di byte che rappresenta il valore della firma.

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue() const
```


## Esempi



Mostra come ottenere il valore di una firma digitale da un documento firmato digitalmente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Digitally signed.docx");

for (auto&& digitalSignature : doc->get_DigitalSignatures())
{
    System::String signatureValue = System::Convert::ToBase64String(digitalSignature->get_SignatureValue());
    ASSERT_EQ(System::String(u"K1cVLLg2kbJRAzT5WK+m++G8eEO+l7S+5ENdjMxxTXkFzGUfvwxREuJdSFj9AbD") + u"MhnGvDURv9KEhC25DDF1al8NRVR71TF3CjHVZXpYu7edQS5/yLw/k5CiFZzCp1+MmhOdYPcVO+Fm" + u"+9fKr2iNLeyYB+fgEeZHfTqTFM2WwAqo=", signatureValue);
}
```

## Vedi anche

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
