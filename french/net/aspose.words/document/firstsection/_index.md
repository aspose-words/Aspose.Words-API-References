---
title: Document.FirstSection
linktitle: FirstSection
articleTitle: FirstSection
second_title: Aspose.Words pour .NET
description: Récupérez facilement la première section de votre document. Optimisez votre flux de travail grâce à notre propriété Document FirstSection pour une organisation simplifiée.
type: docs
weight: 140
url: /fr/net/aspose.words/document/firstsection/
---
## Document.FirstSection property

Obtient la première section du document.

```csharp
public Section FirstSection { get; }
```

## Remarques

Retours`nul`s'il n'y a pas de sections.

## Exemples

Montre comment remplacer du texte dans le pied de page d'un document.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Montre comment créer une nouvelle section avec un générateur de documents.

```csharp
Document doc = new Document();

// Un document vierge contient une section par défaut,
// qui contient des nœuds enfants que nous pouvons éditer.
Assert.AreEqual(1, doc.Sections.Count);

// Utilisez un générateur de documents pour ajouter du texte à la première section.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Créez une deuxième section en insérant un saut de section.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// Chaque section a ses propres paramètres de configuration de page.
// Nous pouvons diviser le texte de la deuxième section en deux colonnes.
// Cela n'affectera pas le texte de la première section.
doc.LastSection.PageSetup.TextColumns.SetCount(2);
builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

Assert.AreEqual(1, doc.FirstSection.PageSetup.TextColumns.Count);
Assert.AreEqual(2, doc.LastSection.PageSetup.TextColumns.Count);

doc.Save(ArtifactsDir + "Section.Create.docx");
```

Montre comment parcourir les enfants d'un nœud composite.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// Une section est un nœud composite et peut contenir des nœuds enfants,
// mais seulement si ces nœuds enfants sont de type nœud « Body » ou « HeaderFooter ».
foreach (Node node in section)
{
    switch (node.NodeType)
    {
        case NodeType.Body:
        {
            Body body = (Body)node;

            Console.WriteLine("Body:");
            Console.WriteLine($"\t\"{body.GetText().Trim()}\"");
            break;
        }
        case NodeType.HeaderFooter:
        {
            HeaderFooter headerFooter = (HeaderFooter)node;

            Console.WriteLine($"HeaderFooter type: {headerFooter.HeaderFooterType}:");
            Console.WriteLine($"\t\"{headerFooter.GetText().Trim()}\"");
            break;
        }
        default:
        {
            throw new Exception("Unexpected node type in a section.");
        }
    }
}
```

### Voir également

* class [Section](../../section/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
