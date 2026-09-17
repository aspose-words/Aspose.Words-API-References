---
title: "Aspose::Words::Math::OfficeMath::get_DisplayType méthode"
linktitle: "get_DisplayType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Math::OfficeMath::get_DisplayType. Obtient/definit le type de format d’affichage Office Math qui indique si une équation est affichée en ligne avec le texte ou sur une ligne séparée en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.math/officemath/get_displaytype/
---
## OfficeMath::get_DisplayType method


Obtient/definit le type de format d’affichage Office [Math](../../) qui indique si une équation est affichée en ligne avec le texte ou sur une ligne séparée.

```cpp
Aspose::Words::Math::OfficeMathDisplayType Aspose::Words::Math::OfficeMath::get_DisplayType()
```

## Remarques


Le type de format d’affichage n’a d’effet que pour le Office [Math](../../) de niveau supérieur.

Le type de format d’affichage retourné est toujours [Inline](../../officemathdisplaytype/) pour les Office [Math](../../) imbriqués.

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

* Enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
