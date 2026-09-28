---
title: "Метод Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator"
linktitle: "GetEnumerator"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator. Возвращает объект перечислителя словаря, который можно использовать для перебора всех элементов в коллекции в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection::GetEnumerator method


Возвращает объект перечислителя словаря, который можно использовать для перебора всех элементов коллекции.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature>>> Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator() override
```


## Примеры



Показывает, как вывести все цифровые подписи подписанного документа.
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

## См. также

* Class [DigitalSignature](../../digitalsignature/)
* Class [DigitalSignatureCollection](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
