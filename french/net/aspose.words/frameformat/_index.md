---
title: FrameFormat Class
linktitle: FrameFormat
articleTitle: FrameFormat
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.FrameFormat pour une mise en forme avancée des cadres dans les paragraphes. Améliorez la conception de vos documents grâce à une intégration fluide et flexible.
type: docs
weight: 3500
url: /fr/net/aspose.words/frameformat/
---
## FrameFormat class

Représente la mise en forme liée au cadre pour un paragraphe.

```csharp
public class FrameFormat
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Height](../../aspose.words/frameformat/height/) { get; } | Obtient la hauteur du cadre spécifié. |
| [HeightRule](../../aspose.words/frameformat/heightrule/) { get; } | Obtient la règle permettant de déterminer la hauteur du cadre spécifié. |
| [HorizontalAlignment](../../aspose.words/frameformat/horizontalalignment/) { get; } | Obtient l'alignement horizontal du cadre spécifié. |
| [HorizontalDistanceFromText](../../aspose.words/frameformat/horizontaldistancefromtext/) { get; } | Obtient la distance horizontale entre un cadre et le texte environnant, en points. |
| [HorizontalPosition](../../aspose.words/frameformat/horizontalposition/) { get; } | Obtient la distance horizontale entre le bord du cadre et l'élément spécifié par le[`RelativeHorizontalPosition`](./relativehorizontalposition/) propriété. |
| [IsFrame](../../aspose.words/frameformat/isframe/) { get; } | Retours`vrai` si le paragraphe est un cadre. |
| [RelativeHorizontalPosition](../../aspose.words/frameformat/relativehorizontalposition/) { get; } | Obtient la position horizontale relative d'un cadre. |
| [RelativeVerticalPosition](../../aspose.words/frameformat/relativeverticalposition/) { get; } | Obtient la position verticale relative d'un cadre. |
| [VerticalAlignment](../../aspose.words/frameformat/verticalalignment/) { get; } | Obtient l'alignement vertical du cadre spécifié. |
| [VerticalDistanceFromText](../../aspose.words/frameformat/verticaldistancefromtext/) { get; } | Spécifie la distance verticale (en points) entre un cadre et le texte environnant. |
| [VerticalPosition](../../aspose.words/frameformat/verticalposition/) { get; } | Obtient la distance verticale entre le bord du cadre et l'élément spécifié par le[`RelativeVerticalPosition`](./relativeverticalposition/) propriété. |
| [Width](../../aspose.words/frameformat/width/) { get; } | Obtient la largeur du cadre spécifié, en points. |

## Remarques

Cet objet est toujours créé. Si un paragraphe est un cadre, toutes les propriétés contiennent leurs valeurs respectives ; sinon, toutes les propriétés sont définies sur leurs valeurs par défaut.

Utiliser[`IsFrame`](./isframe/)pour vérifier si le paragraphe est un cadre.

## Exemples

Montre comment obtenir des informations sur les propriétés de formatage des paragraphes qui sont des cadres.

```csharp
Document doc = new Document(MyDir + "Paragraph frame.docx");

Paragraph paragraphFrame = doc.FirstSection.Body.Paragraphs.OfType<Paragraph>().First(p => p.FrameFormat.IsFrame);

Assert.AreEqual(233.3d, paragraphFrame.FrameFormat.Width);
Assert.AreEqual(138.8d, paragraphFrame.FrameFormat.Height);
Assert.AreEqual(HeightRule.AtLeast, paragraphFrame.FrameFormat.HeightRule);
Assert.AreEqual(HorizontalAlignment.Default, paragraphFrame.FrameFormat.HorizontalAlignment);
Assert.AreEqual(VerticalAlignment.Default, paragraphFrame.FrameFormat.VerticalAlignment);
Assert.AreEqual(34.05d, paragraphFrame.FrameFormat.HorizontalPosition);
Assert.AreEqual(RelativeHorizontalPosition.Page, paragraphFrame.FrameFormat.RelativeHorizontalPosition);
Assert.AreEqual(9.0d, paragraphFrame.FrameFormat.HorizontalDistanceFromText);
Assert.AreEqual(20.5d, paragraphFrame.FrameFormat.VerticalPosition);
Assert.AreEqual(RelativeVerticalPosition.Paragraph, paragraphFrame.FrameFormat.RelativeVerticalPosition);
Assert.AreEqual(0.0d, paragraphFrame.FrameFormat.VerticalDistanceFromText);
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
