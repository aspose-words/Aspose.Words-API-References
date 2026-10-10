---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator metod"
linktitle: "GetEnumerator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator metod. Returnerar ett ordboks‑enumeratorobjekt som kan användas för att iterera över alla objekt i samlingen i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection::GetEnumerator method


Returnerar ett dictionary‑enumeratorobjekt som kan användas för att iterera över alla objekt i samlingen.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature>>> Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator() override
```


## Exempel



Visar hur man skriver ut alla digitala signaturer i ett signerat dokument.
```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_MyDir() + u"Digitally signed.docx");

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature>>> enumerator = digitalSignatures->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature> ds = enumerator->get_Current();

        if (ds != nullptr)
        {
            std::cout << System::ObjectExt::ToString(ds) << std::endl;
        }
    }
}
```

## Se även

* Class [DigitalSignature](../../digitalsignature/)
* Class [DigitalSignatureCollection](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
