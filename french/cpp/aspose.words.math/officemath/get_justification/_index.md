---
title: "Aspose::Words::Math::OfficeMath::get_Justification méthode"
linktitle: "get_Justification"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Math::OfficeMath::get_Justification méthode. Obtient/definit la justification Office Math en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.math/officemath/get_justification/
---
## OfficeMath::get_Justification method


Obtient/definit la justification Office [Math](../../).

```cpp
Aspose::Words::Math::OfficeMathJustification Aspose::Words::Math::OfficeMath::get_Justification()
```

## Remarques


La justification ne peut pas être définie pour l'Office [Math](../../) avec le type de format d'affichage [Inline](../../officemathdisplaytype/).

[Inline](../../../aspose.words/inline/) justification cannot be set to the Office [Math](../../) with display format type [Display](../../officemathdisplaytype/).

Le [DisplayType](../get_displaytype/) correspondant doit être défini avant de définir la justification Office [Math](../../).

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

* Enum [OfficeMathJustification](../../officemathjustification/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
