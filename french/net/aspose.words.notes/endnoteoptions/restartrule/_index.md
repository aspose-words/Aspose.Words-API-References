---
title: EndnoteOptions.RestartRule
second_title: Référence de l'API Aspose.Words pour .NET
description: EndnoteOptions propriété. Détermine quand la numérotation automatique redémarre.
type: docs
weight: 30
url: /fr/net/aspose.words.notes/endnoteoptions/restartrule/
---
## EndnoteOptions.RestartRule property

Détermine quand la numérotation automatique redémarre.

```csharp
public FootnoteNumberingRule RestartRule { get; set; }
```

### Remarques

Toutes les valeurs ne sont pas applicables aux notes de fin. Pour déterminer quelles valeurs sont applicables, voir[`FootnoteNumberingRule`](../../footnotenumberingrule/).

### Exemples

Montre comment redémarrer la numérotation des notes de bas de page/notes de fin à certains endroits du document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les notes de bas de page et de fin sont un moyen d'attacher une référence ou un commentaire secondaire au texte
 // cela n'interfère pas avec le flux du corps principal du texte.
// L'insertion d'une note de bas de page/de fin ajoute un petit symbole de référence en exposant
// au corps du texte principal où nous insérons la note de bas de page/note de fin.
// Chaque note de bas de page/note de fin crée également une entrée, qui consiste en un symbole qui correspond à la référence
// symbole dans le corps du texte principal. Le texte de référence que nous transmettons à la méthode "InsertEndnote" du générateur de documents.
// Les entrées de notes de bas de page, par défaut, apparaissent au bas de chaque page contenant
// leurs symboles de référence et leurs notes de fin apparaissent à la fin du document.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 4.");

builder.InsertBreak(BreakType.PageBreak);

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 4.");

// Par défaut, le symbole de référence pour chaque note de bas de page et note de fin est son index
// parmi toutes les notes de bas de page/notes de fin du document. Chaque document conserve des comptes distincts
// pour les notes de bas de page et de fin et ne redémarre à aucun moment ces décomptes.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// On peut utiliser la propriété "RestartRule" pour faire redémarrer le document
// la note de bas de page/note de fin compte sur une nouvelle page ou section.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Voir également

* enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* class [EndnoteOptions](../)
* espace de noms [Aspose.Words.Notes](../../endnoteoptions/)
* Assemblée [Aspose.Words](../../../)


