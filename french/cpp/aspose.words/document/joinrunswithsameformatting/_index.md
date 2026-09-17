---
title: "Aspose::Words::Document::JoinRunsWithSameFormatting method"
linktitle: "JoinRunsWithSameFormatting"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::JoinRunsWithSameFormatting method. Fusionne les séquences de texte avec le même formatage dans tous les paragraphes du document en C++."
type: docs
weight: 65000
url: /fr/cpp/aspose.words/document/joinrunswithsameformatting/
---
## Document::JoinRunsWithSameFormatting method


Fusionne les séquences avec le même formatage dans tous les paragraphes du document.

```cpp
int32_t Aspose::Words::Document::JoinRunsWithSameFormatting()
```


### ReturnValue

Nombre de fusions effectuées. Lorsque **N** séquences adjacentes sont fusionnées, elles comptent comme **N - 1** fusions.
## Remarques


Il s'agit d'une méthode d'optimisation. Certains documents contiennent des séquences adjacentes avec le même formatage. Cela se produit généralement si un document a été intensivement édité manuellement. Vous pouvez réduire la taille du document et accélérer le traitement ultérieur en fusionnant ces séquences.

L'opération vérifie chaque nœud [Paragraph](../../paragraph/) du document à la recherche de nœuds [Run](../../run/) adjacents possédant des propriétés identiques. Elle ignore les identifiants uniques utilisés pour suivre les sessions d'édition de la création et de la modification des séquences. La première séquence de chaque série de fusion accumule tout le texte. Les séquences restantes sont supprimées du document.

## Exemples



Montre comment fusionner les séquences dans un document afin de réduire les séquences inutiles.
```cpp
// Ouvrez un document contenant des séquences de texte adjacentes avec un formatage identique,
// ce qui se produit couramment si nous modifions plusieurs fois le même paragraphe dans Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Si un nombre quelconque de ces séquences est adjacent avec un formatage identique,
// alors le document peut être simplifié.
ASSERT_EQ(317, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());

// Combinez ces séquences avec cette méthode et vérifiez le nombre de fusions de séquences qui auront lieu.
ASSERT_EQ(121, doc->JoinRunsWithSameFormatting());

// Le nombre de fusions et le nombre de séquences que nous avons après la fusion
// devraient correspondre au nombre de séquences que nous avions initialement.
ASSERT_EQ(196, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
