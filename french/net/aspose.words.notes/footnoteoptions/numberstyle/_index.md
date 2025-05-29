---
title: FootnoteOptions.NumberStyle
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FootnoteOptions NumberStyle pour personnaliser facilement les formats de numérotation des notes de bas de page pour une clarté et un professionnalisme améliorés du document.
type: docs
weight: 20
url: /fr/net/aspose.words.notes/footnoteoptions/numberstyle/
---
## FootnoteOptions.NumberStyle property

Spécifie le format de numérotation pour les notes de bas de page numérotées automatiquement.

```csharp
public NumberStyle NumberStyle { get; set; }
```

## Remarques

Tous les styles de nombre ne sont pas applicables à cette propriété. Pour la liste des styles de nombre applicables, consultez la boîte de dialogue Insérer une note de bas de page ou de fin de document dans Microsoft Word. Si vous sélectionnez un style de nombre non applicable, Microsoft Word rétablira la valeur par défaut.

## Exemples

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

### Voir également

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [FootnoteOptions](../)
* espace de noms [Aspose.Words.Notes](../../../aspose.words.notes/)
* Assemblée [Aspose.Words](../../../)
