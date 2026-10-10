---
title: "Aspose::Words::Shading::get_ForegroundTintAndShade méthode"
linktitle: "get_ForegroundTintAndShade"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Shading::get_ForegroundTintAndShade méthode. Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur de thème de premier plan en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/shading/get_foregroundtintandshade/
---
## Shading::get_ForegroundTintAndShade method


Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur de thème de premier plan.

```cpp
double Aspose::Words::Shading::get_ForegroundTintAndShade()
```

## Remarques


Les valeurs autorisées sont dans la plage de -1 (le plus sombre) à 1 (le plus clair) pour cette propriété.

Zéro (0) est neutre.

## Exemples



Montre comment définir les couleurs de premier plan et d'arrière-plan pour la texture de shading.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Shading> shading = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::Texture12Pt5Percent);
shading->set_ForegroundPatternThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
shading->set_BackgroundPatternThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);

shading->set_ForegroundTintAndShade(0.5);
shading->set_BackgroundTintAndShade(-0.2);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Writeln(u"Foreground and background pattern colors for shading texture.");

doc->Save(get_ArtifactsDir() + u"Font.ForegroundAndBackground.docx");
```

## Voir aussi

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
