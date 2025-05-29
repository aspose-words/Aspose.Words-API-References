---
title: EndnoteOptions.StartNumber
linktitle: StartNumber
articleTitle: StartNumber
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété EndnoteOptions StartNumber améliore votre document en personnalisant les premières notes de fin numérotées pour plus de clarté et d'organisation.
type: docs
weight: 40
url: /fr/net/aspose.words.notes/endnoteoptions/startnumber/
---
## EndnoteOptions.StartNumber property

Spécifie le numéro ou le caractère de départ des premières notes de fin numérotées automatiquement.

```csharp
public int StartNumber { get; set; }
```

## Remarques

Cette propriété n'a d'effet que lorsque[`RestartRule`](../restartrule/)est défini sur Continuous.

## Exemples

Montre comment définir un numéro à partir duquel le document commence le nombre de notes de bas de page/de fin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les notes de bas de page et les notes de fin sont un moyen d'attacher une référence ou un commentaire latéral au texte
 // qui n'interfère pas avec le flux du texte principal.
// L'insertion d'une note de bas de page/de fin ajoute un petit symbole de référence en exposant
// dans le corps du texte principal où nous insérons la note de bas de page/note de fin.
// Chaque note de bas de page/note de fin crée également une entrée, qui se compose d'un symbole
// qui correspond au symbole de référence dans le corps du texte principal.
// Le texte de référence que nous transmettons à la méthode « InsertEndnote » du générateur de documents.
// Les entrées de note de bas de page, par défaut, s'affichent au bas de chaque page qui contient
// leurs symboles de référence et leurs notes de fin s'affichent à la fin du document.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");

// Par défaut, le symbole de référence pour chaque note de bas de page et de fin est son index
// parmi toutes les notes de bas de page et de fin du document. Chaque document conserve un décompte distinct.
// pour les notes de bas de page et pour les notes de fin, qui commencent toutes deux à 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Nous pouvons utiliser la propriété "StartNumber" pour obtenir le document
// commencer un décompte de notes de bas de page ou de fin à un numéro différent.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

### Voir également

* class [EndnoteOptions](../)
* espace de noms [Aspose.Words.Notes](../../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../../)
