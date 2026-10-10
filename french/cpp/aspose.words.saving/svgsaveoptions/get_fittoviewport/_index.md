---
title: "Méthode Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort"
linktitle: "get_FitToViewPort"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort. Indique si le SVG de sortie doit remplir la zone du viewport disponible (fenêtre du navigateur ou conteneur). Lorsqu'elle est définie sur true, la largeur et la hauteur du SVG de sortie sont réglées à 100 %. La valeur par défaut est false en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/svgsaveoptions/get_fittoviewport/
---
## SvgSaveOptions::get_FitToViewPort method


Spécifie si le SVG de sortie doit remplir la zone de visualisation disponible (fenêtre du navigateur ou conteneur). Lorsqu'il est défini sur **true**, la largeur et la hauteur du SVG de sortie sont réglées à 100 %. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort() const
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
