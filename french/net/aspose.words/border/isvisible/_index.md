---
title: Border.IsVisible
linktitle: IsVisible
articleTitle: IsVisible
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété Border IsVisible améliore votre design en renvoyant la valeur true lorsque LineStyle est appliqué. Optimisez votre interface utilisateur grâce à cette fonctionnalité clé !
type: docs
weight: 30
url: /fr/net/aspose.words/border/isvisible/
---
## Border.IsVisible property

Retours`vrai` si le[`LineStyle`](../linestyle/) n'est pasNone .

```csharp
public bool IsVisible { get; }
```

## Exemples

Montre comment supprimer les bordures d'un paragraphe.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Chaque paragraphe possède un ensemble individuel de bordures.
// Nous pouvons accéder aux paramètres d'apparence de ces bordures via l'objet de format de paragraphe.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

 // Nous pouvons supprimer une bordure à la fois en exécutant la méthode ClearFormatting.
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
