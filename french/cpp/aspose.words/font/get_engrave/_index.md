---
title: "Aspose::Words::Font::get_Engrave méthode"
linktitle: "get_Engrave"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_Engrave méthode. Vrai si la police est formatée en gravure en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words/font/get_engrave/
---
## Font::get_Engrave method


Vrai si la police est formatée en gravure.

```cpp
bool Aspose::Words::Font::get_Engrave()
```


## Exemples



Montre comment appliquer des effets de gravure/relief au texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Color(System::Drawing::Color::get_LightBlue());

// Ci-dessous deux façons d'utiliser des ombres pour appliquer un effet 3D au texte.
// 1 -  Graver le texte pour le faire paraître comme si les lettres étaient enfoncées dans la page :
builder->get_Font()->set_Engrave(true);

builder->Writeln(u"This text is engraved.");

// 2 -  Reliever le texte pour le faire paraître comme si les lettres ressortaient de la page :
builder->get_Font()->set_Engrave(false);
builder->get_Font()->set_Emboss(true);

builder->Writeln(u"This text is embossed.");

doc->Save(get_ArtifactsDir() + u"Font.EngraveEmboss.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
