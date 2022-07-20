---
title: FootnoteOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Fournit des options qui contrôlent la numérotation et le positionnement des notes de bas de page dans ce document.
type: docs
weight: 150
url: /fr/net/aspose.words/document/footnoteoptions/
---
## Document.FootnoteOptions property

Fournit des options qui contrôlent la numérotation et le positionnement des notes de bas de page dans ce document.

```csharp
public FootnoteOptions FootnoteOptions { get; }
```

### Exemples

Montre comment sélectionner un endroit différent où le document rassemble et affiche ses notes de bas de page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Une note de bas de page est un moyen d'attacher une référence ou un commentaire latéral au texte
// qui n'interfère pas avec le flux du corps du texte principal.  
// L'insertion d'une note de bas de page ajoute un petit symbole de référence en exposant
// au corps du texte principal où nous insérons la note de bas de page.
// Chaque note de bas de page crée également une entrée en bas de page, constituée d'un symbole
// qui correspond au symbole de référence dans le corps du texte principal.
// Le texte de référence que nous transmettons à la méthode "InsertFootnote" du générateur de document.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Nous pouvons utiliser la propriété "Position" pour déterminer où le document placera toutes ses notes de bas de page.
// Si nous définissons la valeur de la propriété "Position" sur "FootnotePosition.BottomOfPage",
// chaque note de bas de page apparaîtra au bas de la page qui contient sa marque de référence. Ceci est la valeur par défault.
// Si nous définissons la valeur de la propriété "Position" sur "FootnotePosition.BeneathText",
// chaque note de bas de page apparaîtra à la fin du texte de la page qui contient sa marque de référence.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

Montre comment définir un nombre auquel le document commence le décompte des notes de bas de page/notes de fin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les notes de bas de page et les notes de fin sont un moyen d'attacher une référence ou un commentaire latéral au texte
// qui n'interfère pas avec le flux du corps du texte principal. 
// L'insertion d'une note de bas de page/note de fin ajoute un petit symbole de référence en exposant
// au corps du texte principal où nous insérons la note de bas de page/note de fin.
// Chaque note de bas de page/note de fin crée également une entrée, qui consiste en un symbole
// qui correspond au symbole de référence dans le corps du texte principal.
// Le texte de référence que nous transmettons à la méthode "InsertEndnote" du générateur de document.
// Les entrées de note de bas de page, par défaut, s'affichent au bas de chaque page contenant
// leurs symboles de référence et les notes de fin apparaissent à la fin du document.
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
// parmi toutes les notes de bas de page/notes de fin du document. Chaque document maintient des comptes séparés
// pour les notes de bas de page et pour les notes de fin, qui commencent toutes deux à 1.
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// Nous pouvons utiliser la propriété "StartNumber" pour obtenir le document
// commence le décompte d'une note de bas de page ou d'une note de fin à un numéro différent.
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

Montre comment modifier le style de numérotation des marques d'appel de note de bas de page/note de fin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les notes de bas de page et les notes de fin sont un moyen d'attacher une référence ou un commentaire latéral au texte
// qui n'interfère pas avec le flux du corps du texte principal. 
// L'insertion d'une note de bas de page/note de fin ajoute un petit symbole de référence en exposant
// au corps du texte principal où nous insérons la note de bas de page/note de fin.
// Chaque note de bas de page/note de fin crée également une entrée, qui consiste en un symbole correspondant à la référence
// symbole dans le corps du texte principal. Le texte de référence que nous transmettons à la méthode "InsertEndnote" du générateur de document.
// Les entrées de note de bas de page, par défaut, s'affichent au bas de chaque page contenant
// leurs symboles de référence et les notes de fin apparaissent à la fin du document.
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

// Par défaut, le symbole de référence pour chaque note de bas de page et note de fin est son index
// parmi toutes les notes de bas de page/notes de fin du document. Chaque document maintient des comptes séparés
// pour les notes de bas de page et pour les notes de fin. Par défaut, les notes de bas de page affichent leurs numéros en chiffres arabes,
// et les notes de fin affichent leurs numéros en chiffres romains minuscules.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Nous pouvons utiliser la propriété "NumberStyle" pour appliquer des styles de numérotation personnalisés aux notes de bas de page et aux notes de fin.
// Cela n'affectera pas les notes de bas de page/notes de fin avec des marques de référence personnalisées.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

Montre comment redémarrer la numérotation des notes de bas de page/notes de fin à certains endroits du document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les notes de bas de page et les notes de fin sont un moyen d'attacher une référence ou un commentaire latéral au texte
// qui n'interfère pas avec le flux du corps du texte principal. 
// L'insertion d'une note de bas de page/note de fin ajoute un petit symbole de référence en exposant
// au corps du texte principal où nous insérons la note de bas de page/note de fin.
// Chaque note de bas de page/note de fin crée également une entrée, qui consiste en un symbole correspondant à la référence
// symbole dans le corps du texte principal. Le texte de référence que nous transmettons à la méthode "InsertEndnote" du générateur de document.
// Les entrées de note de bas de page, par défaut, s'affichent au bas de chaque page contenant
// leurs symboles de référence et les notes de fin apparaissent à la fin du document.
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
// parmi toutes les notes de bas de page/notes de fin du document. Chaque document maintient des comptes séparés
// pour les notes de bas de page et les notes de fin et ne redémarre à aucun moment ces décomptes.
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// Nous pouvons utiliser la propriété "RestartRule" pour faire redémarrer le document
// la note de bas de page/note de fin compte à une nouvelle page ou section.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### Voir également

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions)
* class [Document](../../document)
* espace de noms [Aspose.Words](../../document)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
