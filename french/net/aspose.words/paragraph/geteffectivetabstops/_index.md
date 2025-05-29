---
title: Paragraph.GetEffectiveTabStops
linktitle: GetEffectiveTabStops
articleTitle: GetEffectiveTabStops
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GetEffectiveTabStops pour récupérer tous les taquets de tabulation d'un paragraphe, y compris ceux des styles et des listes pour une mise en forme améliorée.
type: docs
weight: 270
url: /fr/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

Renvoie un tableau de tous les taquets de tabulation appliqués à ce paragraphe, y compris ceux appliqués indirectement par des styles ou des listes.

```csharp
public TabStop[] GetEffectiveTabStops()
```

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

* class [TabStop](../../tabstop/)
* class [Paragraph](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
