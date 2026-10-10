---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle méthode"
linktitle: "GetByTitle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle méthode. Renvoie la première balise de document structuré rencontrée dans la collection avec le titre spécifié en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection::GetByTitle method


Renvoie la première balise de document structuré rencontrée dans la collection avec le titre spécifié.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle(const System::String &title)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| titre | const System::String\& | Le titre de la balise de document structuré. |
## Remarques


Renvoie null si la balise de document structuré avec le titre spécifié ne peut pas être trouvée.

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

* Interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
