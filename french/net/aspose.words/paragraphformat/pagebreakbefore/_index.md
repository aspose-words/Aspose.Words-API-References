---
title: ParagraphFormat.PageBreakBefore
linktitle: PageBreakBefore
articleTitle: PageBreakBefore
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ParagraphFormat PageBreakBefore, contrôlez facilement les sauts de page avant les paragraphes pour une mise en forme et une lisibilité améliorées du document.
type: docs
weight: 270
url: /fr/net/aspose.words/paragraphformat/pagebreakbefore/
---
## ParagraphFormat.PageBreakBefore property

Vrai si un saut de page est forcé avant le paragraphe.

```csharp
public bool PageBreakBefore { get; set; }
```

## Exemples

Montre comment créer des paragraphes avec des sauts de page au début.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définissez cet indicateur sur « true » pour appliquer un saut de page au début de chaque paragraphe
// que le générateur de documents créera sous cette configuration ParagraphFormat.
// Le premier paragraphe ne recevra pas de saut de page.
// Laissez cet indicateur sur « false » pour démarrer chaque nouveau paragraphe sur la même page
// comme le précédent, à condition qu'il y ait suffisamment d'espace.
builder.ParagraphFormat.PageBreakBefore = pageBreakBefore;

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

LayoutCollector layoutCollector = new LayoutCollector(doc);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

if (pageBreakBefore)
{
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[0]));
    Assert.AreEqual(2, layoutCollector.GetStartPageIndex(paragraphs[1]));
}
else
{
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[0]));
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[1]));
}

doc.Save(ArtifactsDir + "ParagraphFormat.PageBreakBefore.docx");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
