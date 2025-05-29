---
title: HeaderFooter.HeaderFooterType
linktitle: HeaderFooterType
articleTitle: HeaderFooterType
second_title: Aspose.Words pour .NET
description: Découvrez la propriété HeaderFooterType pour accéder et gérer facilement les types d'en-tête et de pied de page de votre document pour un contrôle de mise en forme amélioré.
type: docs
weight: 20
url: /fr/net/aspose.words/headerfooter/headerfootertype/
---
## HeaderFooter.HeaderFooterType property

Obtient le type de cet en-tête/pied de page.

```csharp
public HeaderFooterType HeaderFooterType { get; }
```

## Exemples

Montre comment créer un en-tête et un pied de page.

```csharp
Document doc = new Document();

// Créez un en-tête et ajoutez-y un paragraphe. Le texte de ce paragraphe
// apparaîtra en haut de chaque page de cette section, au-dessus du texte principal.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Créez un pied de page et ajoutez-y un paragraphe. Le texte de ce paragraphe
// apparaîtra au bas de chaque page de cette section, sous le texte principal.
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

* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
