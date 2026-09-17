---
title: "Méthode Aspose::Words::Font::get_Spacing"
linktitle: "get_Spacing"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_Spacing. Retourne ou définit l'espacement (en points) entre les caractères en C++."
type: docs
weight: 40000
url: /fr/cpp/aspose.words/font/get_spacing/
---
## Font::get_Spacing method


Renvoie ou définit l'espacement (en points) entre les caractères.

```cpp
double Aspose::Words::Font::get_Spacing()
```


## Exemples



Montre comment définir l'échelle horizontale et l'espacement des caractères.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ajoutez un segment de texte et augmentez la largeur des caractères à 150 %.
builder->get_Font()->set_Scaling(150);
builder->Writeln(u"Wide characters");

// Ajoutez un segment de texte et ajoutez 1 pt d'espacement horizontal supplémentaire entre chaque caractère.
builder->get_Font()->set_Spacing(1);
builder->Writeln(u"Expanded by 1pt");

// Ajoutez un segment de texte et rapprochez les caractères de 1 pt.
builder->get_Font()->set_Spacing(-1);
builder->Writeln(u"Condensed by 1pt");

doc->Save(get_ArtifactsDir() + u"Font.ScalingSpacing.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
