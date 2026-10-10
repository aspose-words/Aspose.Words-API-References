---
title: "Aspose::Words::PageSetup::get_Margins méthode"
linktitle: "get_Margins"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_Margins méthode. Retourne ou définit les marges prédéfinies de la page en C++."
type: docs
weight: 28000
url: /fr/cpp/aspose.words/pagesetup/get_margins/
---
## PageSetup::get_Margins method


Retourne ou définit les [Margins](../../margins/) prédéfinies de la page.

```cpp
Aspose::Words::Margins Aspose::Words::PageSetup::get_Margins()
```


## Exemples



Indique quand recalculer la mise en page du document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Enregistrer un document au format PDF, en image, ou l'imprimer pour la première fois déclenchera automatiquement
// mise en cache de la mise en page du document dans ses pages.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Modifiez le document d'une certaine manière.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// Dans la version actuelle d'Aspose.Words, la modification du document ne reconstruit pas automatiquement
// la mise en page mise en cache. Si nous souhaitons que la mise en cache
// pour rester à jour, nous devrons la mettre à jour manuellement.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## Voir aussi

* Enum [Margins](../../margins/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
