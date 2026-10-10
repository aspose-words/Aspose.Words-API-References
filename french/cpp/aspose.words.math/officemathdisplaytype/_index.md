---
title: "Aspose::Words::Math::OfficeMathDisplayType enum"
linktitle: "OfficeMathDisplayType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Math::OfficeMathDisplayType enum. Spécifie le type de format d’affichage de l’équation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enum


Spécifie le type de format d'affichage de l'équation.

```cpp
enum class OfficeMathDisplayType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Display | 0 | L’Office [Math](../) est affiché sur sa propre ligne. |
| Inline | 1 | L’Office [Math](../) est affiché en ligne avec le texte. |


## Exemples



Montre comment définir le format d’affichage des Office Math.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Les nœuds OfficeMath qui sont enfants d’autres nœuds OfficeMath sont toujours en ligne.
// Le nœud avec lequel nous travaillons est le nœud de base pour changer son emplacement et son type d’affichage.
ASSERT_EQ(Aspose::Words::Math::MathObjectType::OMathPara, officeMath->get_MathObjectType());
ASSERT_EQ(Aspose::Words::NodeType::OfficeMath, officeMath->get_NodeType());
ASPOSE_ASSERT_EQ(officeMath->get_ParentNode(), officeMath->get_ParentParagraph());

// Changez l’emplacement et le type d’affichage du nœud OfficeMath.
officeMath->set_DisplayType(Aspose::Words::Math::OfficeMathDisplayType::Display);
officeMath->set_Justification(Aspose::Words::Math::OfficeMathJustification::Left);

doc->Save(get_ArtifactsDir() + u"Shape.OfficeMath.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
