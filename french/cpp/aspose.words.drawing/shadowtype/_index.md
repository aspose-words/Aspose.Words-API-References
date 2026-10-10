---
title: "Aspose::Words::Drawing::ShadowType énum"
linktitle: "ShadowType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShadowType énum. Spécifie le type d'ombre d'une forme en C++."
type: docs
weight: 35000
url: /fr/cpp/aspose.words.drawing/shadowtype/
---
## ShadowType enum


Spécifie le type d’ombre d’une forme.

```cpp
enum class ShadowType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| ShadowMixed | -2 | Aucun des préréglages d'ombre prédéfinis. |
| Shadow1 | 1 | Premier type d'ombre. |
| Shadow10 | 10 | Dixième type d'ombre. |
| Shadow11 | 11 | Onzième type d'ombre. |
| Shadow12 | 12 | Douzième type d'ombre. |
| Shadow13 | 13 | Treizième type d'ombre. |
| Shadow14 | 14 | Quatorzième type d'ombre. |
| Shadow15 | 15 | Quinzième type d'ombre. |
| Shadow16 | 16 | Seizième type d'ombre. |
| Shadow17 | 17 | Dix-septième type d'ombre. |
| Shadow18 | 18 | Dix-huitième type d'ombre. |
| Shadow19 | 19 | Dix-neuvième type d'ombre. |
| Shadow2 | 2 | Deuxième type d'ombre. |
| Shadow20 | 20 | Vingtième type d'ombre. |
| Shadow21 | 21 | Vingt-et-unième type d'ombre. |
| Shadow22 | 22 | Vingt‑deuxième type d'ombre. |
| Shadow23 | 23 | Vingt‑troisième type d'ombre. |
| Shadow24 | 24 | Vingt‑quatrième type d'ombre. |
| Shadow25 | 25 | Vingt‑cinquième type d'ombre. |
| Shadow26 | 26 | Vingt‑sixième type d'ombre. |
| Shadow27 | 27 | Vingt‑septième type d'ombre. |
| Shadow28 | 28 | Vingt‑huitième type d'ombre. |
| Shadow29 | 29 | Vingt‑neuvième type d'ombre. |
| Shadow3 | 3 | Troisième type d'ombre. |
| Shadow30 | 30 | Trentième type d'ombre. |
| Shadow31 | 31 | Trente‑premier type d'ombre. |
| Shadow32 | 32 | Trente‑deuxième type d'ombre. |
| Shadow33 | 33 | Trente‑troisième type d'ombre. |
| Shadow34 | 34 | Trente‑quatrième type d'ombre. |
| Shadow35 | 35 | Trente‑cinquième type d'ombre. |
| Shadow36 | 36 | Trente‑sixième type d'ombre. |
| Shadow37 | 37 | Trente‑septième type d'ombre. |
| Shadow38 | 38 | Trente‑huitième type d'ombre. |
| Shadow39 | 39 | Trente‑neuvième type d'ombre. |
| Shadow4 | 4 | Quatrième type d'ombre. |
| Shadow40 | 40 | Quarantième type d'ombre. |
| Shadow41 | 41 | Quarante‑premier type d'ombre. |
| Shadow42 | 42 | Quarante‑deuxième type d'ombre. |
| Shadow43 | 43 | Quarante‑troisième type d'ombre. |
| Shadow5 | 5 | Cinquième type d'ombre. |
| Shadow6 | 6 | Sixième type d'ombre. |
| Shadow7 | 7 | Septième type d'ombre. |
| Shadow8 | 8 | Huitième type d'ombre. |
| Shadow9 | 9 | Neuvième type d'ombre. |


## Exemples



Montre comment travailler avec le format d'ombre pour la forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

if (shape->get_ShadowFormat()->get_Visible() && shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::Shadow2)
{
    shape->get_ShadowFormat()->set_Type(Aspose::Words::Drawing::ShadowType::Shadow7);
}

if (shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::ShadowMixed)
{
    shape->get_ShadowFormat()->Clear();
}
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
