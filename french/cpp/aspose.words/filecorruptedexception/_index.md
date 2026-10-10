---
title: "Aspose::Words::FileCorruptedException typedef"
linktitle: "FileCorruptedException"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::FileCorruptedException typedef. Lancé lors du chargement du document, lorsque le document semble corrompu et impossible à charger. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 133000
url: /fr/cpp/aspose.words/filecorruptedexception/
---
## FileCorruptedException typedef


Lancé lors du chargement du document, lorsque le document semble corrompu et impossible à charger. Pour en savoir plus, consultez l'article de documentation [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
using Aspose::Words::FileCorruptedException = typedef System::ExceptionWrapper<Details_FileCorruptedException>
```


## Exemples



Montre comment intercepter une FileCorruptedException.
```cpp
try
{
    // Si nous obtenons le message d'erreur "Unreadable content" en essayant d'ouvrir un document avec Microsoft Word,
    // il est probable que nous obtenions une exception lors de la tentative de chargement de ce document avec Aspose.Words.
    auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted document.docx");
}
catch (Aspose::Words::FileCorruptedException& e)
{
    std::cout << e->get_Message() << std::endl;
}
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
