---
title: Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator method
linktitle: GetEnumerator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator method. Returns a dictionary enumerator object that can be used to iterate over all items in the collection in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection::GetEnumerator method


Returns a dictionary enumerator object that can be used to iterate over all items in the collection.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature>>> Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator() override
```


## Examples



Shows how to print all the digital signatures of a signed document. 
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

## See Also

* Class [DigitalSignature](../../digitalsignature/)
* Class [DigitalSignatureCollection](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
