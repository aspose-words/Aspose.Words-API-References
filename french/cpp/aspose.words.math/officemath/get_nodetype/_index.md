---
title: "Aspose::Words::Math::OfficeMath::get_NodeType méthode"
linktitle: "get_NodeType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Math::OfficeMath::get_NodeType méthode. Retourne OfficeMath en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.math/officemath/get_nodetype/
---
## OfficeMath::get_NodeType method


Retourne [OfficeMath](../../../aspose.words/nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::Math::OfficeMath::get_NodeType() const override
```


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

* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
