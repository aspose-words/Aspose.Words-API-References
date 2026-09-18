---
title: "Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue Methode"
linktitle: "get_SignatureValue"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue Methode. Gibt ein Byte-Array zurück, das einen Signaturwert in C++ darstellt."
type: docs
weight: 6500
url: /de/cpp/aspose.words.digitalsignatures/digitalsignature/get_signaturevalue/
---
## DigitalSignature::get_SignatureValue method


Ermittelt ein Byte-Array, das einen Signaturwert darstellt.

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::DigitalSignatures::DigitalSignature::get_SignatureValue() const
```


## Beispiele



Zeigt, wie man einen digitalen Signaturwert aus einem digital signierten Dokument erhält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Digitally signed.docx");

for (auto&& digitalSignature : doc->get_DigitalSignatures())
{
    System::String signatureValue = System::Convert::ToBase64String(digitalSignature->get_SignatureValue());
    ASSERT_EQ(System::String(u"K1cVLLg2kbJRAzT5WK+m++G8eEO+l7S+5ENdjMxxTXkFzGUfvwxREuJdSFj9AbD") + u"MhnGvDURv9KEhC25DDF1al8NRVR71TF3CjHVZXpYu7edQS5/yLw/k5CiFZzCp1+MmhOdYPcVO+Fm" + u"+9fKr2iNLeyYB+fgEeZHfTqTFM2WwAqo=", signatureValue);
}
```

## Siehe auch

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
