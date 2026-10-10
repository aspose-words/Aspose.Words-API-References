---
title: "Méthode Aspose::Words::Document::get_OriginalLoadFormat"
linktitle: "get_OriginalLoadFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_OriginalLoadFormat method. Obtient le format du document original qui a été chargé dans cet objet en C++."
type: docs
weight: 41000
url: /fr/cpp/aspose.words/document/get_originalloadformat/
---
## Document::get_OriginalLoadFormat method


Obtient le format du document original qui a été chargé dans cet objet.

```cpp
Aspose::Words::LoadFormat Aspose::Words::Document::get_OriginalLoadFormat() const
```

## Remarques


Si vous avez créé un nouveau document vierge, renvoie la valeur [Doc](../../loadformat/).

## Exemples



Montre comment récupérer les détails de l'opération de chargement d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```

## Voir aussi

* Enum [LoadFormat](../../loadformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
