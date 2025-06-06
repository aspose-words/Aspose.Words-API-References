---
title: BorderCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words pour .NET
description: Découvrez comment la méthode BorderCollection ClearFormatting supprime sans effort toutes les bordures d'objets, améliorant ainsi votre conception avec des visuels nets et précis.
type: docs
weight: 140
url: /fr/net/aspose.words/bordercollection/clearformatting/
---
## BorderCollection.ClearFormatting method

Supprime toutes les bordures d'un objet.

```csharp
public void ClearFormatting()
```

## Exemples

Montre comment supprimer toutes les bordures de tous les paragraphes d'un document.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Le premier paragraphe de ce document a des bordures visibles avec ces paramètres.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), firstParagraphBorders.Color.ToArgb());
Assert.AreEqual(LineStyle.Single, firstParagraphBorders.LineStyle);
Assert.AreEqual(3.0d, firstParagraphBorders.LineWidth);

// Utilisez la méthode « ClearFormatting » sur chaque paragraphe pour supprimer toutes les bordures.
foreach (Paragraph paragraph in doc.FirstSection.Body.Paragraphs)
{
    paragraph.ParagraphFormat.Borders.ClearFormatting();

    foreach (Border border in paragraph.ParagraphFormat.Borders)
    {
        Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
        Assert.AreEqual(LineStyle.None, border.LineStyle);
        Assert.AreEqual(0.0d, border.LineWidth);
    }
}

doc.Save(ArtifactsDir + "BorderCollection.RemoveAllBorders.docx");
```

### Voir également

* class [BorderCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
