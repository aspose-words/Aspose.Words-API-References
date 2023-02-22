---
title: BorderCollection.Equals
second_title: Référence de l'API Aspose.Words pour .NET
description: BorderCollection méthode. Compare les collections de bordures.
type: docs
weight: 150
url: /fr/net/aspose.words/bordercollection/equals/
---
## BorderCollection.Equals method

Compare les collections de bordures.

```csharp
public bool Equals(BorderCollection brColl)
```

### Exemples

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

// Après avoir changé le style de ligne des bordures dans le deuxième paragraphe seulement,
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
* espace de noms [Aspose.Words](../../bordercollection/)
* Assemblée [Aspose.Words](../../../)


