---
title: "Aspose::Words::Document::UpdatePageLayout méthode"
linktitle: "UpdatePageLayout"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::UpdatePageLayout méthode. Reconstruit la mise en page du document en C++."
type: docs
weight: 98000
url: /fr/cpp/aspose.words/document/updatepagelayout/
---
## Document::UpdatePageLayout method


Reconstruit la mise en page du document.

```cpp
void Aspose::Words::Document::UpdatePageLayout()
```

## Remarques


Cette méthode formate un document en pages et met à jour les champs liés aux numéros de page dans le document tels que PAGE, PAGES, PAGEREF et REF. Les informations de mise en page à jour sont nécessaires pour un rendu correct du document vers des formats à pages fixes.

Cette méthode est invoquée automatiquement lors de la première conversion d'un document en PDF, XPS, image ou lors de son impression. Cependant, si vous modifiez le document après le rendu et essayez de le rendre à nouveau, Aspose.Words ne mettra pas à jour la mise en page automatiquement. Dans ce cas, vous devez appeler [UpdatePageLayout](./) avant de rendre à nouveau.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
