---
title: Paragraph.ParentStory
second_title: Référence de l'API Aspose.Words pour .NET
description: Paragraph propriété. Récupère lhistoire au niveau de la section parent qui peut êtreBody ouHeaderFooter .
type: docs
weight: 210
url: /fr/net/aspose.words/paragraph/parentstory/
---
## Paragraph.ParentStory property

Récupère l'histoire au niveau de la section parent qui peut être[`Body`](../../body/) ou[`HeaderFooter`](../../headerfooter/) .

```csharp
public Story ParentStory { get; }
```

### Exemples

Montre comment créer un en-tête et un pied de page.

```csharp
Document doc = new Document();

// Crée un en-tête et y ajoute un paragraphe. Le texte de ce paragraphe
// apparaîtra en haut de chaque page de cette section, au-dessus du corps du texte principal.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Crée un pied de page et y ajoute un paragraphe. Le texte de ce paragraphe
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

* class [Story](../../story/)
* class [Paragraph](../)
* espace de noms [Aspose.Words](../../paragraph/)
* Assemblée [Aspose.Words](../../../)


