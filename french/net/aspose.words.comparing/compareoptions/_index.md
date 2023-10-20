---
title: CompareOptions Class
linktitle: CompareOptions
articleTitle: CompareOptions
second_title: Aspose.Words pour .NET
description: Aspose.Words.Comparing.CompareOptions classe. Permet de choisir les options avancées pour lopération de comparaison de documents en C#.
type: docs
weight: 270
url: /fr/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

Permet de choisir les options avancées pour l'opération de comparaison de documents.

Pour en savoir plus, visitez le[Comparer des documents](https://docs.aspose.com/words/net/compare-documents/) article documentaire.

```csharp
public class CompareOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [CompareOptions](compareoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [CompareMoves](../../aspose.words.comparing/compareoptions/comparemoves/) { get; set; } | Spécifie s'il faut comparer les différences dansMoveRevision entre les deux documents. Par défaut, les révisions de déplacement ne sont pas produites. |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity/) { get; set; } | Spécifie si les modifications sont suivies par caractère ou par mot. La valeur par défaut estWordLevel . |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges/) { get; set; } | True indique que la comparaison des documents n'est pas sensible à la casse. Par défaut, la comparaison est sensible à la casse. |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments/) { get; set; } | Spécifie s'il faut comparer les différences dans les commentaires. Par défaut, les commentaires ne sont pas ignorés. |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/compareoptions/ignoredmluniqueid/) { get; set; } | Spécifie s'il faut ignorer la différence dans l'ID unique de DrawingML. La valeur par défaut est`FAUX` . |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields/) { get; set; } | Spécifie s'il faut comparer les différences dans les champs. Par défaut, les champs ne sont pas ignorés. |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes/) { get; set; } | Spécifie s'il faut comparer les différences entre les notes de bas de page et les notes de fin. Par défaut, les notes de bas de page ne sont pas ignorées. |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting/) { get; set; } | True indique que le formatage est ignoré. Par défaut, le formatage du document n'est pas ignoré. |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters/) { get; set; } | True indique que le contenu des en-têtes et des pieds de page est ignoré. Par défaut, les en-têtes et les pieds de page ne sont pas ignorés. |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables/) { get; set; } | Spécifie s'il faut comparer les différences dans les données contenues dans les tableaux. Par défaut, les tableaux ne sont pas ignorés. |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes/) { get; set; } | Spécifie s'il faut comparer les différences dans les données contenues dans les zones de texte. Par défaut, les zones de texte ne sont pas ignorées. |
| [Target](../../aspose.words.comparing/compareoptions/target/) { get; set; } | Spécifie quel document doit être utilisé comme cible lors de la comparaison. |

## Exemples

Montre comment filtrer des types spécifiques d’éléments de document lors d’une comparaison.

```csharp
// Créez le document original et remplissez-le avec différents types d'éléments.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Texte du paragraphe référencé par une note de fin :
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// Tableau:
builder.StartTable();
builder.InsertCell();
builder.Write("Original cell 1 text");
builder.InsertCell();
builder.Write("Original cell 2 text");
builder.EndTable();

// Zone de texte:
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

// Entête:
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

// La comparaison de documents crée une révision pour chaque modification du document édité.
// Un objet CompareOptions possède une série d'indicateurs qui peuvent supprimer les révisions
// sur chaque type d'élément respectif, ignorant effectivement leur changement.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreFormatting = false;
compareOptions.IgnoreCaseChanges = false;
compareOptions.IgnoreComments = false;
compareOptions.IgnoreTables = false;
compareOptions.IgnoreFields = false;
compareOptions.IgnoreFootnotes = false;
compareOptions.IgnoreTextboxes = false;
compareOptions.IgnoreHeadersAndFooters = false;
compareOptions.Target = ComparisonTargetType.New;

docOriginal.Compare(docEdited, "John Doe", DateTime.Now, compareOptions);
docOriginal.Save(ArtifactsDir + "Document.CompareOptions.docx");
```

### Voir également

* espace de noms [Aspose.Words.Comparing](../../aspose.words.comparing/)
* Assemblée [Aspose.Words](../../)
