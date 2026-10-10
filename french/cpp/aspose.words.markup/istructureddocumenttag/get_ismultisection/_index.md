---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection méthode"
linktitle: "get_IsMultiSection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection. Retourne true si cette instance est une balise de document structuré à portée (multi-section) en C++."
type: docs
weight: 3500
url: /fr/cpp/aspose.words.markup/istructureddocumenttag/get_ismultisection/
---
## IStructuredDocumentTag::get_IsMultiSection method


Renvoie true si cette instance est une balise de document structuré à portée (multi-section).

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection()=0
```


## Exemples



Montre comment obtenir une balise de document structuré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags by id.docx");

// Obtenez la balise de document structuré par Id.
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt = doc->get_Range()->get_StructuredDocumentTags()->GetById(1160505028);
std::cout << System::Convert::ToString(sdt->get_IsMultiSection()) << std::endl;
std::cout << sdt->get_Title() << std::endl;

// Obtenez la balise de document structuré ou la balise de plage par Titre.
sdt = doc->get_Range()->get_StructuredDocumentTags()->GetByTitle(u"Alias4");
std::cout << sdt->get_Id() << std::endl;
```

## Voir aussi

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
