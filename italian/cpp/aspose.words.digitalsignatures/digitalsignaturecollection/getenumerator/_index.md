---
title: "Metodo Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator"
linktitle: "GetEnumerator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator. Restituisce un oggetto enumeratore del dizionario che può essere usato per iterare su tutti gli elementi della collezione in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection::GetEnumerator method


Restituisce un oggetto enumeratore di dizionario che può essere usato per iterare su tutti gli elementi della collezione.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature>>> Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator() override
```


## Esempi



Mostra come stampare tutte le firme digitali di un documento firmato.
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

## Vedi anche

* Class [DigitalSignature](../../digitalsignature/)
* Class [DigitalSignatureCollection](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
