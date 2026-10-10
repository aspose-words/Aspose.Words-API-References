---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title méthode"
linktitle: "get_Title"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title méthode. Spécifie le nom convivial associé à ce SDT. Ne peut pas être nul en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.markup/istructureddocumenttag/get_title/
---
## IStructuredDocumentTag::get_Title method


Spécifie le nom convivial associé à ce **SDT**. Ne peut pas être null.

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_Title() const =0
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
