---
title: "Méthode Aspose::Words::Font::get_Italic"
linktitle: "get_Italic"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_Italic. Vrai si la police est formatée en italique en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words/font/get_italic/
---
## Font::get_Italic method


Vrai si la police est formatée en italique.

```cpp
bool Aspose::Words::Font::get_Italic()
```


## Exemples



Montre comment écrire du texte en italique à l'aide d'un DocumentBuilder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Italic(true);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Italic.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
