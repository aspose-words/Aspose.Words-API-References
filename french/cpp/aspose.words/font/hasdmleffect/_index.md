---
title: "Méthode Aspose::Words::Font::HasDmlEffect"
linktitle: "HasDmlEffect"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::HasDmlEffect. Vérifie si un effet de texte DrawingML particulier est appliqué en C++."
type: docs
weight: 58000
url: /fr/cpp/aspose.words/font/hasdmleffect/
---
## Font::HasDmlEffect method


Vérifie si un effet de texte DrawingML particulier est appliqué.

```cpp
bool Aspose::Words::Font::HasDmlEffect(Aspose::Words::TextDmlEffect dmlEffectType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| dmlEffectType | Aspose::Words::TextDmlEffect | Type d'effet de texte DrawingML. |

### ReturnValue

**true** if particular DrawingML text effect is applied.

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

* Enum [TextDmlEffect](../../textdmleffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
