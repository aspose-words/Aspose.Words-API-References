---
title: "Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue método"
linktitle: "get_SignatureValue"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue método. Obtiene una matriz de bytes que representa un valor de firma en C++."
type: docs
weight: 6500
url: /es/cpp/aspose.words.digitalsignatures/digitalsignature/get_signaturevalue/
---
## DigitalSignature::get_SignatureValue method


Obtiene una matriz de bytes que representa el valor de la firma.

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue() const
```


## Ejemplos



Muestra cómo obtener el valor de una firma digital de un documento firmado digitalmente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Digitally signed.docx");

for (auto&& digitalSignature : doc->get_DigitalSignatures())
{
    System::String signatureValue = System::Convert::ToBase64String(digitalSignature->get_SignatureValue());
    ASSERT_EQ(System::String(u"K1cVLLg2kbJRAzT5WK+m++G8eEO+l7S+5ENdjMxxTXkFzGUfvwxREuJdSFj9AbD") + u"MhnGvDURv9KEhC25DDF1al8NRVR71TF3CjHVZXpYu7edQS5/yLw/k5CiFZzCp1+MmhOdYPcVO+Fm" + u"+9fKr2iNLeyYB+fgEeZHfTqTFM2WwAqo=", signatureValue);
}
```

## Ver también

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
