---
title: "Aspose::Words::TextDmlEffect enum"
linktitle: "TextDmlEffect"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TextDmlEffect enum. Effet de texte Dml pour les segments de texte en C++."
type: docs
weight: 122000
url: /fr/cpp/aspose.words/textdmleffect/
---
## TextDmlEffect enum


Effet de texte Dml pour les segments de texte.

```cpp
enum class TextDmlEffect
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Glow | 0 | Effet de lueur, dans lequel un contour flou de couleur est ajouté à l'extérieur des bords de l'objet. |
| Fill | 1 | Effet de superposition de remplissage. |
| Shadow | 2 | Effet d'ombre. |
| Outline | 3 | Effet de contour. |
| Effect3D | 4 | Effet 3D. |
| Reflection | 5 | Effet de réflexion. |


## Exemples



Montre comment vérifier si un segment affiche un effet de texte DrawingML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DrawingML text effects.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_TRUE(runs->idx_get(0)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(1)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(2)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Reflection));
ASSERT_TRUE(runs->idx_get(3)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Effect3D));
ASSERT_TRUE(runs->idx_get(4)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Fill));
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
