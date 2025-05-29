---
title: Border.GetHashCode
linktitle: GetHashCode
articleTitle: GetHashCode
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Border GetHashCode, une puissante fonction de hachage qui améliore l'intégrité des données et les performances de vos applications. Libérez son potentiel dès aujourd'hui !
type: docs
weight: 110
url: /fr/net/aspose.words/border/gethashcode/
---
## Border.GetHashCode method

Sert de fonction de hachage pour ce type.

```csharp
public override int GetHashCode()
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

* class [Border](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
