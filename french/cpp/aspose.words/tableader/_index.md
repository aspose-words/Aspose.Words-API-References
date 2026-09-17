---
title: "Aspose::Words::TabLeader enum"
linktitle: "TabLeader"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TabLeader enum. Spécifie le type de la ligne de repère affichée sous le caractère de tabulation en C++."
type: docs
weight: 121000
url: /fr/cpp/aspose.words/tableader/
---
## TabLeader enum


Spécifie le type de la ligne de repère affichée sous le caractère de tabulation.

```cpp
enum class TabLeader
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Aucune ligne de repère n'est affichée. |
| Points | 1 | La ligne de repère est composée de points. |
| Tirets | 2 | La ligne de repère est composée de tirets. |
| Ligne | 3 | La ligne de repère est une ligne unique. |
| Épais | 4 | La ligne de repère est une ligne épaisse unique. |
| MiddleDot | 5 | La ligne de repère est composée de points-milieu. |


## Exemples



Montre comment définir des arrêts de tabulation personnalisés pour un paragraphe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Si nous sommes dans un paragraphe sans arrêts de tabulation dans cette collection,
// le curseur sautera de 36 points chaque fois que nous appuyons sur la touche Tab dans Microsoft Word.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetEffectiveTabStops()->get_Length());

// Nous pouvons ajouter des arrêts de tabulation personnalisés dans Microsoft Word si nous activons la règle via l'onglet "Affichage".
// Chaque unité de cette règle correspond à deux arrêts de tabulation par défaut, soit 72 points.
// Nous pouvons ajouter des arrêts de tabulation personnalisés par programmation comme ceci.
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_TabStops();
tabStops->Add(72, Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dots);
tabStops->Add(216, Aspose::Words::TabAlignment::Center, Aspose::Words::TabLeader::Dashes);
tabStops->Add(360, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Line);

// Nous pouvons voir ces arrêts de tabulation dans Microsoft Word en activant la règle via "Affichage" -> "Afficher" -> "Règle".
ASSERT_EQ(3, para->GetEffectiveTabStops()->get_Length());

// Tout caractère de tabulation que nous ajoutons utilisera les arrêts de tabulation sur la règle et peut,
// selon la valeur du leader de tabulation, laisser une ligne entre le départ et l'arrivée de la tabulation.
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"\tTab 1\tTab 2\tTab 3"));

doc->Save(get_ArtifactsDir() + u"Paragraph.TabStops.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
