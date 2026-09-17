---
title: "Méthode Aspose::Words::Document::RemoveBlankPages"
linktitle: "RemoveBlankPages"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Document::RemoveBlankPages. Supprime les pages blanches du document en C++."
type: docs
weight: 67500
url: /fr/cpp/aspose.words/document/removeblankpages/
---
## Document::RemoveBlankPages method


Supprime les pages blanches du document.

```cpp
System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::Document::RemoveBlankPages()
```


### ReturnValue

La liste des numéros de page a été considérée comme vide et supprimée.

## Exemples



Montre comment supprimer les pages vierges du document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Blank pages.docx");
ASSERT_EQ(2, doc->get_PageCount());
doc->RemoveBlankPages();
doc->UpdatePageLayout();
ASSERT_EQ(1, doc->get_PageCount());
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
