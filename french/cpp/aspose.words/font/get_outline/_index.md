---
title: "Aspose::Words::Font::get_Outline méthode"
linktitle: "get_Outline"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_Outline méthode. Vrai si la police est formatée en contour en C++."
type: docs
weight: 31000
url: /fr/cpp/aspose.words/font/get_outline/
---
## Font::get_Outline method


Vrai si la police est formatée en contour.

```cpp
bool Aspose::Words::Font::get_Outline()
```


## Exemples



Montre comment créer un segment de texte formaté en contour.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Définissez le drapeau Outline pour changer la couleur de remplissage du texte en blanc et
// laissez un fin contour autour de chaque caractère dans la couleur originale du texte.
builder->get_Font()->set_Outline(true);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has an outline.");

doc->Save(get_ArtifactsDir() + u"Font.Outline.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
