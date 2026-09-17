---
title: "Aspose::Words::Shading::get_BackgroundPatternThemeColor méthode"
linktitle: "get_BackgroundPatternThemeColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Shading::get_BackgroundPatternThemeColor méthode. Obtient ou définit la couleur du thème du motif d'arrière-plan dans le schéma de couleurs appliqué qui est associé à cet objet Shading en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/shading/get_backgroundpatternthemecolor/
---
## Shading::get_BackgroundPatternThemeColor method


Obtient ou définit la couleur du thème du motif d'arrière-plan dans le schéma de couleurs appliqué qui est associé à cet objet [Shading](../).

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Shading::get_BackgroundPatternThemeColor()
```


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

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
