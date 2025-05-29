---
title: TabAlignment Enum
linktitle: TabAlignment
articleTitle: TabAlignment
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.TabAlignment pour un alignement personnalisable des taquets de tabulation. Améliorez la mise en forme de vos documents avec précision et flexibilité dès aujourd'hui !
type: docs
weight: 7030
url: /fr/net/aspose.words/tabalignment/
---
## TabAlignment enumeration

Spécifie l'alignement/le type d'un taquet de tabulation.

```csharp
public enum TabAlignment
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Left | `0` | Aligne à gauche le texte après le taquet de tabulation. |
| Center | `1` | Centre le texte autour du taquet de tabulation. |
| Right | `2` | Aligne le texte à droite au niveau du taquet de tabulation. |
| Decimal | `3` | Aligne le texte sur le point décimal. |
| Bar | `4` | Dessine une barre verticale à la position de la tabulation. |
| List | `6` | La tabulation est un délimiteur entre le numéro/la puce et le texte dans un élément de liste. |
| Clear | `7` | Efface tout taquet de tabulation dans cette position. |

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
