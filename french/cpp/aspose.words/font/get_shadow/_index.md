---
title: "Aspose::Words::Font::get_Shadow méthode"
linktitle: "get_Shadow"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_Shadow méthode. Vrai si la police est formatée avec une ombre en C++."
type: docs
weight: 35000
url: /fr/cpp/aspose.words/font/get_shadow/
---
## Font::get_Shadow method


Vrai si la police est formatée avec une ombre.

```cpp
bool Aspose::Words::Font::get_Shadow()
```


## Exemples



Montre comment créer un segment de texte formaté avec une ombre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Définissez le drapeau Shadow pour appliquer un effet d'ombre décalée,
// ce qui donne l'impression que les lettres flottent au-dessus de la page.
builder->get_Font()->set_Shadow(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has a shadow.");

doc->Save(get_ArtifactsDir() + u"Font.Shadow.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
