---
title: PageSetup.EndnoteOptions
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words pour .NET
description: PageSetup EndnoteOptions propriété. Fournit des options qui contrôlent la numérotation et le positionnement des notes de fin dans cette section en C#.
type: docs
weight: 120
url: /fr/net/aspose.words/pagesetup/endnoteoptions/
---
## PageSetup.EndnoteOptions property

Fournit des options qui contrôlent la numérotation et le positionnement des notes de fin dans cette section.

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

## Exemples

Montre comment configurer les options affectant les notes de bas de page/notes de fin dans une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote reference text.");

// Configurez toutes les notes de bas de page de la première section pour redémarrer la numérotation à partir de 1
// à chaque nouvelle page et s'affichent directement sous le texte sur chaque page.
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// Configurez toutes les notes de fin de la première section pour maintenir un décompte continu tout au long de la section,
// à partir de 1. Définissez-les également tous pour qu'ils apparaissent collectés à la fin du document.
EndnoteOptions endnoteOptions = doc.Sections[0].PageSetup.EndnoteOptions;
endnoteOptions.Position = EndnotePosition.EndOfDocument;
endnoteOptions.RestartRule = FootnoteNumberingRule.Continuous;
endnoteOptions.StartNumber = 1;

doc.Save(ArtifactsDir + "PageSetup.FootnoteOptions.docx");
```

### Voir également

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
