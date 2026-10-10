---
title: "Aspose::Words::Font::get_Scaling méthode"
linktitle: "get_Scaling"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_Scaling méthode. Obtient ou définit le facteur d'échelle de la largeur des caractères en pourcentage en C++."
type: docs
weight: 33000
url: /fr/cpp/aspose.words/font/get_scaling/
---
## Font::get_Scaling method


Obtient ou définit le redimensionnement de la largeur des caractères en pourcentage.

```cpp
int32_t Aspose::Words::Font::get_Scaling()
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
