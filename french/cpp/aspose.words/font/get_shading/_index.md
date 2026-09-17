---
title: "Aspose::Words::Font::get_Shading méthode"
linktitle: "get_Shading"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_Shading méthode. Retourne un objet Shading qui fait référence au formatage d'ombrage pour la police en C++."
type: docs
weight: 34000
url: /fr/cpp/aspose.words/font/get_shading/
---
## Font::get_Shading method


Renvoie un objet [Ombrage](../../shading/) qui se réfère au format d'ombrage de la police.

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::Font::get_Shading()
```


## Exemples



Montre comment appliquer un ombrage au texte créé par un générateur de documents.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Color(System::Drawing::Color::get_White());

// Une façon de rendre le texte créé avec notre couleur de police blanche visible
// est d'appliquer un effet d'ombrage d'arrière-plan.
System::SharedPtr<Aspose::Words::Shading> shading = builder->get_Font()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalUp);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_OrangeRed());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"White text on an orange background with a two-tone texture.");

doc->Save(get_ArtifactsDir() + u"Font.Shading.docx");
```

## Voir aussi

* Class [Shading](../../shading/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
