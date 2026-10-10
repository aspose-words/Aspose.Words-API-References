---
title: "Méthode Aspose::Words::Font::get_UnderlineColor"
linktitle: "get_UnderlineColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_UnderlineColor. Obtient ou définit la couleur du soulignement appliqué à la police en C++."
type: docs
weight: 56000
url: /fr/cpp/aspose.words/font/get_underlinecolor/
---
## Font::get_UnderlineColor method


Obtient ou définit la couleur du soulignement appliqué à la police.

```cpp
System::Drawing::Color Aspose::Words::Font::get_UnderlineColor()
```


## Exemples



Montre comment configurer le style et la couleur d'un soulignement de texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Aspose::Words::Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
