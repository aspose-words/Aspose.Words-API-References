---
title: "Aspose::Words::Math::OfficeMathJustification enum"
linktitle: "OfficeMathJustification"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Math::OfficeMathJustification enum. Spécifie la justification de l'équation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enum


Spécifie l'alignement de l'équation.

```cpp
enum class OfficeMathJustification
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| CenterGroup | 1 | Justifie les instances de texte mathématique à gauche les unes par rapport aux autres, et centre le groupe de texte mathématique (le [Math](../)[Paragraph](../../aspose.words/paragraph/)) par rapport à la page. |
| Centre | 2 | Centre chaque instance de texte mathématique individuellement par rapport aux marges. |
| Left | 3 | Justification à gauche du [Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Right | 4 | Justification à droite du [Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Inline | 7 | Position [Inline](../../aspose.words/inline/) du [Math](../). |
| Default | n/a | Valeur par défaut [CenterGroup](./). |


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
