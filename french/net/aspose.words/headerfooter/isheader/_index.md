---
title: HeaderFooter.IsHeader
second_title: Référence de l'API Aspose.Words pour .NET
description: HeaderFooter propriété. Vrai si ceciHeaderFooter lobjet est un entête.
type: docs
weight: 30
url: /fr/net/aspose.words/headerfooter/isheader/
---
## HeaderFooter.IsHeader property

Vrai si ceci[`HeaderFooter`](../) l'objet est un en-tête.

```csharp
public bool IsHeader { get; }
```

### Exemples

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

* class [HeaderFooter](../)
* espace de noms [Aspose.Words](../../headerfooter/)
* Assemblée [Aspose.Words](../../../)


