---
title: Document.EndnoteOptions
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words pour .NET
description: Explorez la propriété EndnoteOptions pour personnaliser la numérotation et le positionnement des notes de fin, améliorant ainsi la clarté et le professionnalisme de votre document.
type: docs
weight: 120
url: /fr/net/aspose.words/document/endnoteoptions/
---
## Document.EndnoteOptions property

Fournit des options qui contrôlent la numérotation et le positionnement des notes de fin dans ce document.

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

## Exemples

Montre comment sélectionner un emplacement différent où le document collecte et affiche ses notes de fin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Une note de fin est un moyen d'attacher une référence ou un commentaire latéral au texte
 // qui n'interfère pas avec le flux du texte principal.
// L'insertion d'une note de fin ajoute un petit symbole de référence en exposant
// dans le corps du texte principal où nous insérons la note de fin.
// Chaque note de fin crée également une entrée à la fin du document, composée d'un symbole
// qui correspond au symbole de référence dans le corps du texte principal.
// Le texte de référence que nous transmettons à la méthode « InsertEndnote » du générateur de documents.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Nous pouvons utiliser la propriété « Position » pour déterminer où le document placera toutes ses notes de fin.
// Si nous définissons la valeur de la propriété "Position" sur "EndnotePosition.EndOfDocument",
// Chaque note de bas de page apparaîtra dans une collection à la fin du document. Il s'agit de la valeur par défaut.
// Si nous définissons la valeur de la propriété « Position » sur « EndnotePosition.EndOfSection »,
// chaque note de bas de page apparaîtra dans une collection à la fin de la section dont le texte contient la marque de référence de la note de fin.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

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

Montre comment modifier le style de numérotation des marques de référence de note de bas de page/de fin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les notes de bas de page et les notes de fin sont un moyen d'attacher une référence ou un commentaire latéral au texte
 // qui n'interfère pas avec le flux du texte principal.
// L'insertion d'une note de bas de page/de fin ajoute un petit symbole de référence en exposant
// dans le corps du texte principal où nous insérons la note de bas de page/note de fin.
// Chaque note de bas de page/note de fin crée également une entrée, qui consiste en un symbole correspondant à la référence
// Symbole dans le corps du texte. Texte de référence transmis à la méthode « InsertEndnote » du générateur de documents.
// Les entrées de note de bas de page, par défaut, s'affichent au bas de chaque page qui contient
// leurs symboles de référence et leurs notes de fin s'affichent à la fin du document.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// Par défaut, le symbole de référence pour chaque note de bas de page et de fin est son index
// parmi toutes les notes de bas de page et de fin du document. Chaque document conserve un décompte distinct.
// pour les notes de bas de page et les notes de fin. Par défaut, les notes de bas de page affichent leur numéro en chiffres arabes.
// et les notes de fin affichent leurs numéros en chiffres romains minuscules.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Nous pouvons utiliser la propriété « NumberStyle » pour appliquer des styles de numérotation personnalisés aux notes de bas de page et aux notes de fin.
// Cela n'affectera pas les notes de bas de page/notes de fin avec des marques de référence personnalisées.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Montre comment redémarrer la numérotation des notes de bas de page/de fin à certains endroits du document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les notes de bas de page et les notes de fin sont un moyen d'attacher une référence ou un commentaire latéral au texte
 // qui n'interfère pas avec le flux du texte principal.
// L'insertion d'une note de bas de page/de fin ajoute un petit symbole de référence en exposant
// dans le corps du texte principal où nous insérons la note de bas de page/note de fin.
// Chaque note de bas de page/note de fin crée également une entrée, qui consiste en un symbole correspondant à la référence
// Symbole dans le corps du texte. Texte de référence transmis à la méthode « InsertEndnote » du générateur de documents.
// Les entrées de note de bas de page, par défaut, s'affichent au bas de chaque page qui contient
// leurs symboles de référence et leurs notes de fin s'affichent à la fin du document.
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

// Par défaut, le symbole de référence pour chaque note de bas de page et de fin est son index
// parmi toutes les notes de bas de page et de fin du document. Chaque document conserve un décompte distinct.
// pour les notes de bas de page et les notes de fin et ne redémarre pas ces décomptes à aucun moment.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Nous pouvons utiliser la propriété « RestartRule » pour que le document redémarre
// la note de bas de page/de fin compte sur une nouvelle page ou section.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Voir également

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
