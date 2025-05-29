---
title: CompareOptions.IgnoreTextboxes
linktitle: IgnoreTextboxes
articleTitle: IgnoreTextboxes
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété CompareOptions IgnoreTextboxes améliore la comparaison des données en excluant les différences de zone de texte pour des résultats plus précis.
type: docs
weight: 120
url: /fr/net/aspose.words.comparing/compareoptions/ignoretextboxes/
---
## CompareOptions.IgnoreTextboxes property

Spécifie s'il faut comparer les différences dans les données contenues dans les zones de texte.

```csharp
public bool IgnoreTextboxes { get; set; }
```

## Remarques

Par défaut, les zones de texte ne sont pas ignorées.

## Exemples

Montre comment filtrer des types spécifiques d'éléments de document lors d'une comparaison.

```csharp
// Créez le document original et remplissez-le avec différents types d'éléments.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Texte du paragraphe référencé avec une note de fin :
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// Tableau:
builder.StartTable();
builder.InsertCell();
builder.Write("Original cell 1 text");
builder.InsertCell();
builder.Write("Original cell 2 text");
builder.EndTable();

// Zone de texte :
Shape textBox = builder.InsertShape(ShapeType.TextBox, 150, 20);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("Original textbox contents");

// Champ DATE :
builder.MoveTo(docOriginal.FirstSection.Body.AppendParagraph(""));
builder.InsertField(" DATE ");

// Commentaire:
Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", DateTime.Now);
newComment.SetText("Original comment.");
builder.CurrentParagraph.AppendChild(newComment);

// En-tête :
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Original header contents.");

// Créez un clone de notre document et effectuez une modification rapide sur chacun des éléments du document cloné.
Document docEdited = (Document)docOriginal.Clone(true);
Paragraph firstParagraph = docEdited.FirstSection.Body.FirstParagraph;

firstParagraph.Runs[0].Text = "hello world! this is the first paragraph, after editing.";
firstParagraph.ParagraphFormat.Style = docEdited.Styles[StyleIdentifier.Heading1];
((Footnote)docEdited.GetChild(NodeType.Footnote, 0, true)).FirstParagraph.Runs[1].Text = "Edited endnote text.";
((Table)docEdited.GetChild(NodeType.Table, 0, true)).FirstRow.Cells[1].FirstParagraph.Runs[0].Text = "Edited Cell 2 contents";
((Shape)docEdited.GetChild(NodeType.Shape, 0, true)).FirstParagraph.Runs[0].Text = "Edited textbox contents";
((FieldDate)docEdited.Range.Fields[0]).UseLunarCalendar = true;
((Comment)docEdited.GetChild(NodeType.Comment, 0, true)).FirstParagraph.Runs[0].Text = "Edited comment.";
docEdited.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].FirstParagraph.Runs[0].Text =
    "Edited header contents.";

// La comparaison de documents crée une révision pour chaque modification dans le document modifié.
// Un objet CompareOptions possède une série d'indicateurs qui peuvent supprimer les révisions
// sur chaque type d'élément respectif, ignorant ainsi efficacement leur changement.
CompareOptions compareOptions = new CompareOptions
{
    CompareMoves = false,
    IgnoreFormatting = false,
    IgnoreCaseChanges = false,
    IgnoreComments = false,
    IgnoreTables = false,
    IgnoreFields = false,
    IgnoreFootnotes = false,
    IgnoreTextboxes = false,
    IgnoreHeadersAndFooters = false,
    Target = ComparisonTargetType.New
};

docOriginal.Compare(docEdited, "John Doe", DateTime.Now, compareOptions);
docOriginal.Save(ArtifactsDir + "Revision.CompareOptions.docx");
```

### Voir également

* class [CompareOptions](../)
* espace de noms [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* Assemblée [Aspose.Words](../../../)
