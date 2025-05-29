---
title: TabLeader Enum
linktitle: TabLeader
articleTitle: TabLeader
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.TabLeader, définissant les styles de ligne de repère pour les onglets, améliorant la mise en forme et la lisibilité des documents dans vos projets.
type: docs
weight: 7040
url: /fr/net/aspose.words/tableader/
---
## TabLeader enumeration

Spécifie le type de ligne de repère affichée sous le caractère de tabulation.

```csharp
public enum TabLeader
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Aucune ligne de repère n'est affichée. |
| Dots | `1` | La ligne de repère est composée de points. |
| Dashes | `2` | La ligne de repère est composée de tirets. |
| Line | `3` | La ligne de repère est une ligne unique. |
| Heavy | `4` | La ligne de repère est une seule ligne épaisse. |
| MiddleDot | `5` | La ligne de repère est composée de points centraux. |

## Exemples

Montre comment définir des taquets de tabulation personnalisés pour un paragraphe.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Si nous sommes dans un paragraphe sans tabulation dans cette collection,
// le curseur sautera de 36 points à chaque fois que nous appuierons sur la touche Tab dans Microsoft Word.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// Nous pouvons ajouter des taquets de tabulation personnalisés dans Microsoft Word si nous activons la règle via l'onglet « Affichage ».
// Chaque unité sur cette règle correspond à deux taquets de tabulation par défaut, soit 72 points.
// Nous pouvons ajouter des tabulations personnalisées par programmation comme ceci.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// Nous pouvons voir ces taquets de tabulation dans Microsoft Word en activant la règle via « Affichage » -> « Afficher » -> « Règle ».
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Tous les caractères de tabulation que nous ajoutons utiliseront les taquets de tabulation sur la règle et pourront,
// en fonction de la valeur du leader de l'onglet, laissez une ligne entre les destinations de départ et d'arrivée de l'onglet.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
