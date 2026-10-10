---
title: "Énumération Aspose::Words::Saving::SvgTextOutputMode"
linktitle: "SvgTextOutputMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énumération Aspose::Words::Saving::SvgTextOutputMode. Permet de spécifier comment le texte d'un document doit être rendu lors de l'enregistrement au format SVG en C++."
type: docs
weight: 83000
url: /fr/cpp/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enum


Permet de spécifier comment le texte à l'intérieur d'un document doit être rendu lors de l'enregistrement au format SVG.

```cpp
enum class SvgTextOutputMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| UseSvgFonts | 0 | Les polices SVG sont utilisées pour rendre le texte. Notez que tous les navigateurs ne prennent pas en charge les polices SVG. |
| UseTargetMachineFonts | 1 | [Fonts](../../aspose.words.fonts/) installées sur la machine cible sont utilisées pour rendre le texte. Notez que si certaines des polices utilisées dans le document ne sont pas disponibles sur la machine cible, le document peut apparaître différemment. |
| UsePlacedGlyphs | 2 | Le texte est rendu à l'aide de courbes. Notez que la sélection du texte ne fonctionnera pas si vous utilisez cette option. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
