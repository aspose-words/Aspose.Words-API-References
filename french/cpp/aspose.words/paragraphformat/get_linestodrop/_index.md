---
title: "Aspose::Words::ParagraphFormat::get_LinesToDrop méthode"
linktitle: "get_LinesToDrop"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::get_LinesToDrop méthode. Obtient ou définit le nombre de lignes du texte du paragraphe utilisées pour calculer la hauteur de la lettrine en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words/paragraphformat/get_linestodrop/
---
## ParagraphFormat::get_LinesToDrop method


Obtient ou définit le nombre de lignes du texte du paragraphe utilisées pour calculer la hauteur de la lettrine.

```cpp
int32_t Aspose::Words::ParagraphFormat::get_LinesToDrop()
```


## Exemples



Montre comment définir la taille d’une lettrine.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modifiez la propriété \"LinesToDrop\" pour désigner un paragraphe comme lettrine,
// qui le transformera en une grande majuscule qui décorera le paragraphe suivant.
// Attribuez à cette propriété la valeur 4 pour donner à la lettrine la hauteur de quatre lignes de texte.
builder->get_ParagraphFormat()->set_LinesToDrop(4);
builder->Writeln(u"H");

// Réinitialisez la propriété \"LinesToDrop\" à 0 pour transformer le paragraphe suivant en un paragraphe ordinaire.
// Le texte de ce paragraphe s'enroulera autour de la lettrine.
builder->get_ParagraphFormat()->set_LinesToDrop(0);
builder->Writeln(u"ello world!");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LinesToDrop.odt");
```

## Voir aussi

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
