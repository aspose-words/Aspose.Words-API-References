---
title: "Méthode Aspose::Words::Font::get_Hidden"
linktitle: "get_Hidden"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_Hidden. Vrai si la police est formatée comme texte masqué en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words/font/get_hidden/
---
## Font::get_Hidden method


Vrai si la police est formatée comme texte masqué.

```cpp
bool Aspose::Words::Font::get_Hidden()
```


## Exemples



Montre comment créer un segment de texte masqué.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Avec le drapeau Hidden réglé sur true, tout texte que nous créons avec cet objet Font sera invisible dans le document.
// Nous ne verrons pas ou ne mettrons pas en surbrillance le texte masqué à moins d'activer l'option "Texte masqué"
// trouvé dans Microsoft Word via "Fichier" -> "Options" -> "Affichage". Le texte sera toujours présent,
// et nous pourrons accéder à ce texte par programmation.
// Il n'est pas recommandé d'utiliser cette méthode pour masquer des informations sensibles.
builder->get_Font()->set_Hidden(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text will not be visible in the document.");

doc->Save(get_ArtifactsDir() + u"Font.Hidden.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
