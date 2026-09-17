---
title: "Aspose::Words::Rendering::PageInfo::get_Colored méthode"
linktitle: "get_Colored"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Rendering::PageInfo::get_Colored méthode. Retourne true si la page contient du contenu en couleur en C++."
type: docs
weight: 1500
url: /fr/cpp/aspose.words.rendering/pageinfo/get_colored/
---
## PageInfo::get_Colored method


Renvoie **true** si la page contient du contenu coloré.

```cpp
bool Aspose::Words::Rendering::PageInfo::get_Colored()
```


## Exemples



Montre comment vérifier si la page est en couleur ou non.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Vérifiez que la première page du document n'est pas colorée.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## Voir aussi

* Class [PageInfo](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
