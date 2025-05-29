---
title: BorderCollection.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words pour .NET
description: Découvrez la méthode BorderCollection Equals pour comparer efficacement des collections de bordures et améliorer votre productivité de codage. Optimisez vos projets dès aujourd'hui !
type: docs
weight: 150
url: /fr/net/aspose.words/bordercollection/equals/
---
## BorderCollection.Equals method

Compare des collections de bordures.

```csharp
public bool Equals(BorderCollection brColl)
```

## Exemples

Montre comment les collections de bordures peuvent partager des éléments.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// Puisque nous avons utilisé la même configuration de bordure lors de la création
// ces paragraphes, leurs collections de bordures partagent les mêmes éléments.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
BorderCollection secondParagraphBorders = builder.CurrentParagraph.ParagraphFormat.Borders;
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsTrue(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());
    Assert.False(firstParagraphBorders[i].IsVisible);
}

foreach (Border border in secondParagraphBorders)
    border.LineStyle = LineStyle.DotDash;

// Après avoir modifié le style de ligne des bordures dans le deuxième paragraphe seulement,
// les collections de bordures ne partagent plus les mêmes éléments.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // Changer l'apparence d'une bordure vide la rend visible.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### Voir également

* class [BorderCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
