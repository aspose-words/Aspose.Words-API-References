---
title: "Aspose::Words::Document::GetPageInfo méthode"
linktitle: "GetPageInfo"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::GetPageInfo méthode. Obtient la taille de la page, l'orientation et d'autres informations sur une page qui peuvent être utiles pour l'impression ou le rendu en C++."
type: docs
weight: 62000
url: /fr/cpp/aspose.words/document/getpageinfo/
---
## Document::GetPageInfo method


Obtient la taille de la page, l'orientation et d'autres informations sur une page qui pourraient être utiles pour l'impression ou le rendu.

```cpp
System::SharedPtr<Aspose::Words::Rendering::PageInfo> Aspose::Words::Document::GetPageInfo(int32_t pageIndex)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| pageIndex | int32_t | L'index de page basé sur zéro. |

## Exemples



Montre comment vérifier si la page est en couleur ou non.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Vérifiez que la première page du document n'est pas colorée.
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## Voir aussi

* Class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
