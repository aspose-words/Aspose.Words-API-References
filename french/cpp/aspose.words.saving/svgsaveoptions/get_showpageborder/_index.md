---
title: "Méthode Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder"
linktitle: "get_ShowPageBorder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder. Contrôle si une bordure est ajoutée au contour de la page. La valeur par défaut est true en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.saving/svgsaveoptions/get_showpageborder/
---
## SvgSaveOptions::get_ShowPageBorder method


Contrôle si une bordure est ajoutée au contour de la page. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder() const
```


## Exemples



Montre comment imiter les propriétés des images lors de la conversion d'un document .docx en .svg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Configurez l'objet SvgSaveOptions pour enregistrer sans bordures de page ni texte sélectionnable.
auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_FitToViewPort(true);
options->set_ShowPageBorder(false);
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.SaveLikeImage.svg", options);
```

## Voir aussi

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
