---
title: Story.AppendParagraph
linktitle: AppendParagraph
articleTitle: AppendParagraph
second_title: Aspose.Words pour .NET
description: Story AppendParagraph méthode. Une méthode de raccourci qui crée unParagraph objet avec du texte facultatif et lajoute à la fin de cet objet en C#.
type: docs
weight: 60
url: /fr/net/aspose.words/story/appendparagraph/
---
## Story.AppendParagraph method

Une méthode de raccourci qui crée un[`Paragraph`](../../paragraph/) objet avec du texte facultatif et l'ajoute à la fin de cet objet.

```csharp
public Paragraph AppendParagraph(string text)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| text | String | Le texte du paragraphe. Peut être`nul` ou une chaîne vide. |

### Return_Value

Le paragraphe nouvellement créé et ajouté.

## Exemples

Montre comment créer un en-tête et un pied de page.

```csharp
Document doc = new Document();

// Créez un en-tête et ajoutez-y un paragraphe. Le texte de ce paragraphe
// apparaîtra en haut de chaque page de cette section, au-dessus du corps du texte principal.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Créez un pied de page et ajoutez-y un paragraphe. Le texte de ce paragraphe
// apparaîtra au bas de chaque page de cette section, sous le corps du texte principal.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Voir également

* class [Paragraph](../../paragraph/)
* class [Story](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
