---
title: FootnoteOptions Class
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: Aspose.Words pour .NET
description: Aspose.Words.Notes.FootnoteOptions classe. Représente les options de numérotation des notes de bas de page pour un document ou une section en C#.
type: docs
weight: 4280
url: /fr/net/aspose.words.notes/footnoteoptions/
---
## FootnoteOptions class

Représente les options de numérotation des notes de bas de page pour un document ou une section.

Pour en savoir plus, visitez le[Travailler avec les notes de bas de page et de fin](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) article documentaire.

```csharp
public sealed class FootnoteOptions
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Columns](../../aspose.words.notes/footnoteoptions/columns/) { get; set; } | Spécifie le nombre de colonnes avec lesquelles la zone des notes de bas de page est formatée. |
| [NumberStyle](../../aspose.words.notes/footnoteoptions/numberstyle/) { get; set; } | Spécifie le format numérique pour les notes de bas de page numérotées automatiquement. |
| [Position](../../aspose.words.notes/footnoteoptions/position/) { get; set; } | Spécifie la position des notes de bas de page. |
| [RestartRule](../../aspose.words.notes/footnoteoptions/restartrule/) { get; set; } | Détermine quand la numérotation automatique redémarre. |
| [StartNumber](../../aspose.words.notes/footnoteoptions/startnumber/) { get; set; } | Spécifie le numéro ou le caractère de départ des premières notes de bas de page numérotées automatiquement. |

## Exemples

Montre comment diviser la section de note de bas de page en un nombre donné de colonnes.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

Montre comment sélectionner un emplacement différent où le document collecte et affiche ses notes de bas de page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Une note de bas de page est un moyen d'attacher une référence ou un commentaire secondaire au texte
 // cela n'interfère pas avec le flux du corps principal du texte.
// L'insertion d'une note de bas de page ajoute un petit symbole de référence en exposant
// au corps du texte principal où nous insérons la note de bas de page.
// Chaque note de bas de page crée également une entrée en bas de page, constituée d'un symbole
// qui correspond au symbole de référence dans le corps du texte principal.
// Le texte de référence que nous transmettons à la méthode "InsertFootnote" du générateur de documents.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Nous pouvons utiliser la propriété "Position" pour déterminer où le document placera toutes ses notes de bas de page.
// Si on fixe la valeur de la propriété "Position" à "FootnotePosition.BottomOfPage",
// chaque note de bas de page apparaîtra au bas de la page contenant sa marque de référence. Ceci est la valeur par défault.
// Si on fixe la valeur de la propriété "Position" à "FootnotePosition.BeneathText",
// chaque note de bas de page apparaîtra à la fin du texte de la page contenant sa marque de référence.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

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

Montre comment modifier le style numérique des marques de référence de note de bas de page/note de fin.

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
// parmi toutes les notes de bas de page/notes de fin du document. Chaque document conserve des comptes distincts
// pour les notes de bas de page et pour les notes de fin. Par défaut, les notes de bas de page affichent leurs numéros en chiffres arabes,
// et les notes de fin affichent leurs numéros en chiffres romains minuscules.
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// Nous pouvons utiliser la propriété "NumberStyle" pour appliquer des styles de numérotation personnalisés aux notes de bas de page et de fin.
// Cela n'affectera pas les notes de bas de page/notes de fin avec des marques de référence personnalisées.
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

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

* property [FootnoteOptions](../../aspose.words/document/footnoteoptions/)
* property [FootnoteOptions](../../aspose.words/pagesetup/footnoteoptions/)
* espace de noms [Aspose.Words.Notes](../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../)
