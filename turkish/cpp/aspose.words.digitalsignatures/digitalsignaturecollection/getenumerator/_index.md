---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator yöntemi"
linktitle: "GetEnumerator"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator yöntemi. Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir sözlük enumeratör nesnesi döndürür C++'ta."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection::GetEnumerator method


Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir sözlük enumeratör nesnesi döndürür.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature>>> Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator() override
```


## Örnekler



İmzalı bir belgenin tüm dijital imzalarını nasıl yazdırılacağını gösterir.
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

## Ayrıca Bakınız

* Class [DigitalSignature](../../digitalsignature/)
* Class [DigitalSignatureCollection](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
