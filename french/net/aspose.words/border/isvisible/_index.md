---
title: Border.IsVisible
linktitle: IsVisible
articleTitle: IsVisible
second_title: Aspose.Words pour .NET
description: Border IsVisible propriété. Retoursvrai si laLineStyle nest pasNone  en C#.
type: docs
weight: 30
url: /fr/net/aspose.words/border/isvisible/
---
## Border.IsVisible property

Retours`vrai` si la[`LineStyle`](../linestyle/) n'est pasNone .

```csharp
public bool IsVisible { get; }
```

## Exemples

Montre comment supprimer les bordures d’un paragraphe.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Chaque paragraphe a un ensemble individuel de bordures.
// On peut accéder aux paramètres d'apparence de ces bordures via l'objet format paragraphe.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

 // Nous pouvons supprimer une bordure d'un coup en exécutant la méthode ClearFormatting.
// L'exécution de cette méthode sur chaque bordure d'un paragraphe supprimera toutes ses bordures.
foreach (Border border in borders)
    border.ClearFormatting();

Assert.AreEqual(Color.Empty.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(0.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.None, borders[0].LineStyle);
Assert.IsFalse(borders[0].IsVisible);

doc.Save(ArtifactsDir + "Border.ClearFormatting.docx");
```

### Voir également

* class [Border](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
