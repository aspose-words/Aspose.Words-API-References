---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator método"
linktitle: "GetEnumerator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator método. Devuelve un objeto enumerador de diccionario que puede usarse para iterar sobre todos los elementos de la colección en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection::GetEnumerator method


Devuelve un objeto enumerador de diccionario que puede usarse para iterar sobre todos los elementos de la colección.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature>>> Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator() override
```


## Ejemplos



Muestra cómo imprimir todas las firmas digitales de un documento firmado.
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

## Ver también

* Class [DigitalSignature](../../digitalsignature/)
* Class [DigitalSignatureCollection](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
