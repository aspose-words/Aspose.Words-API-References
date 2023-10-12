---
title: FootnoteOptions.StartNumber
second_title: Référence de l'API Aspose.Words pour .NET
description: FootnoteOptions propriété. Spécifie le numéro ou le caractère de départ des premières notes de bas de page numérotées automatiquement.
type: docs
weight: 50
url: /fr/net/aspose.words.notes/footnoteoptions/startnumber/
---
## FootnoteOptions.StartNumber property

Spécifie le numéro ou le caractère de départ des premières notes de bas de page numérotées automatiquement.

```csharp
public int StartNumber { get; set; }
```

### Remarques

Cette propriété n'a d'effet que lorsque[`RestartRule`](../restartrule/) est défini sur Continuous.

### Exemples

Montre comment définir un numéro à partir duquel le document commence le décompte des notes de bas de page/notes de fin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les notes de bas de page et de fin sont un moyen d'attacher une référence ou un commentaire secondaire au texte
 // cela n'interfère pas avec le flux du corps principal du texte.
// L'insertion d'une note de bas de page/de fin ajoute un petit symbole de référence en exposant
// au corps du texte principal où nous insérons la note de bas de page/note de fin.
// Chaque note de bas de page/note de fin crée également une entrée, qui consiste en un symbole
// qui correspond au symbole de référence dans le corps du texte principal.
// Le texte de référence que nous transmettons à la méthode "InsertEndnote" du générateur de documents.
// Les entrées de notes de bas de page, par défaut, apparaissent au bas de chaque page contenant
// leurs symboles de référence et leurs notes de fin apparaissent à la fin du document.
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

// Par défaut, le symbole de référence pour chaque note de bas de page et note de fin est son index
// parmi toutes les notes de bas de page/notes de fin du document. Chaque document conserve des comptes distincts
// pour les notes de bas de page et pour les notes de fin, qui commencent toutes deux par 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Nous pouvons utiliser la propriété "StartNumber" pour amener le document
// commence le décompte d'une note de bas de page ou d'une note de fin à un numéro différent.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

### Voir également

* class [FootnoteOptions](../)
* espace de noms [Aspose.Words.Notes](../../footnoteoptions/)
* Assemblée [Aspose.Words](../../../)


