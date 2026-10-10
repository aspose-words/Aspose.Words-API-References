---
title: "Méthode Aspose::Words::Document::get_PageCount"
linktitle: "get_PageCount"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Document::get_PageCount. Obtient le nombre de pages du document tel que calculé par la dernière opération de mise en page en C++."
type: docs
weight: 43000
url: /fr/cpp/aspose.words/document/get_pagecount/
---
## Document::get_PageCount method


Obtient le nombre de pages du document tel que calculé par la dernière opération de mise en page.

```cpp
int32_t Aspose::Words::Document::get_PageCount()
```


## Exemples



Montre comment compter le nombre de pages du document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Vérifiez le nombre de pages attendu du document.
ASSERT_EQ(3, doc->get_PageCount());

// L'obtention de la propriété PageCount a déclenché la mise en page du document pour calculer la valeur.
// Cette opération n'aura pas besoin d'être refaite lors du rendu du document vers un format de sauvegarde à page fixe,
// comme le .pdf. Vous pouvez ainsi gagner du temps, surtout avec des documents plus complexes.
doc->Save(get_ArtifactsDir() + u"Document.GetPageCount.pdf");
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
