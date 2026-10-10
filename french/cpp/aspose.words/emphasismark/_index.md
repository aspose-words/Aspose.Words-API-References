---
title: "Aspose::Words::EmphasisMark enum"
linktitle: "EmphasisMark"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::EmphasisMark enum. Spécifie les types possibles de marques d'emphase en C++."
type: docs
weight: 89000
url: /fr/cpp/aspose.words/emphasismark/
---
## EmphasisMark enum


Spécifie les types possibles de marque d'emphase.

```cpp
enum class EmphasisMark
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Aucune marque d'emphase. |
| OverSolidCircle | 1 | La marque d'emphase est un cercle noir plein affiché au-dessus du texte. |
| OverComma | 2 | La marque d'emphase est un caractère virgule affiché au-dessus du texte. |
| OverWhiteCircle | 3 | La marque d'emphase est un cercle blanc vide affiché au-dessus du texte. |
| UnderSolidCircle | 4 | La marque d'emphase est un cercle noir plein affiché en dessous du texte. |


## Exemples



Montre comment ajouter un caractère supplémentaire rendu au-dessus/en dessous du glyphe.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Types possibles de marque d'emphase :
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder->get_Font()->set_EmphasisMark(emphasisMark);

builder->Write(u"Emphasis text");
builder->Writeln();
builder->get_Font()->ClearFormatting();
builder->Write(u"Simple text");

builder->get_Document()->Save(get_ArtifactsDir() + u"Fonts.SetEmphasisMark.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
