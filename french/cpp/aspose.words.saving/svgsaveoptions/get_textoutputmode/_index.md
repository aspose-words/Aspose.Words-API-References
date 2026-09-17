---
title: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode méthode"
linktitle: "get_TextOutputMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode méthode. Obtient ou définit une valeur déterminant comment le texte doit être rendu en SVG en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.saving/svgsaveoptions/get_textoutputmode/
---
## SvgSaveOptions::get_TextOutputMode method


Obtient ou définit une valeur déterminant comment le texte doit être rendu dans le SVG.

```cpp
Aspose::Words::Saving::SvgTextOutputMode Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode() const
```

## Remarques


Utilisez cette propriété pour obtenir ou définir le mode de rendu du texte à l'intérieur d'un document lors de l'enregistrement au format SVG.

La valeur par défaut est [UseTargetMachineFonts](../../svgtextoutputmode/).

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

* Enum [SvgTextOutputMode](../../svgtextoutputmode/)
* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
