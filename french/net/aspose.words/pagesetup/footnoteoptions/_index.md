---
title: PageSetup.FootnoteOptions
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: Aspose.Words pour .NET
description: Découvrez les options de note de bas de page de PageSetup pour personnaliser facilement la numérotation et le positionnement des notes de bas de page pour une clarté et un professionnalisme améliorés du document.
type: docs
weight: 150
url: /fr/net/aspose.words/pagesetup/footnoteoptions/
---
## PageSetup.FootnoteOptions property

Fournit des options qui contrôlent la numérotation et le positionnement des notes de bas de page dans cette section.

```csharp
public FootnoteOptions FootnoteOptions { get; }
```

## Exemples

Montre comment configurer les options affectant les notes de bas de page/notes de fin dans une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote reference text.");

// Configurer toutes les notes de bas de page de la première section pour redémarrer la numérotation à partir de 1
// à chaque nouvelle page et s'affichent directement sous le texte sur chaque page.
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// Configurez toutes les notes de fin de la première section pour maintenir un décompte continu tout au long de la section,
// à partir de 1. Définissez-les également tous pour qu'ils apparaissent rassemblés à la fin du document.
EndnoteOptions endnoteOptions = doc.Sections[0].PageSetup.EndnoteOptions;
endnoteOptions.Position = EndnotePosition.EndOfDocument;
endnoteOptions.RestartRule = FootnoteNumberingRule.Continuous;
endnoteOptions.StartNumber = 1;

doc.Save(ArtifactsDir + "PageSetup.FootnoteOptions.docx");
```

### Voir également

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
