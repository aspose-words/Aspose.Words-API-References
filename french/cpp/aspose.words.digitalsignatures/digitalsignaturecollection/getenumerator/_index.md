---
title: "Méthode Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator"
linktitle: "GetEnumerator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator. Retourne un objet énumérateur de dictionnaire qui peut être utilisé pour parcourir tous les éléments de la collection en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection::GetEnumerator method


Renvoie un objet énumérateur de dictionnaire qui peut être utilisé pour parcourir tous les éléments de la collection.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature>>> Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator() override
```


## Exemples



Montre comment imprimer toutes les signatures numériques d'un document signé.
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

## Voir aussi

* Class [DigitalSignature](../../digitalsignature/)
* Class [DigitalSignatureCollection](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
