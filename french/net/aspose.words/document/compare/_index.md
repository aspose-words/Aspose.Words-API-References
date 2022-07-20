---
title: Compare
second_title: Référence de l'API Aspose.Words pour .NET
description: Compare ce document avec un autre document produisant des modifications en nombre de révisions dédition et de formatRevisionaspose.words/revision .
type: docs
weight: 540
url: /fr/net/aspose.words/document/compare/
---
## Compare(Document, string, DateTime) {#compare}

Compare ce document avec un autre document produisant des modifications en nombre de révisions d'édition et de format[`Revision`](../../revision) .

```csharp
public void Compare(Document document, string author, DateTime dateTime)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| document | Document | Document à comparer. |
| author | String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | DateTime | La date et l'heure à utiliser pour les révisions. |

### Remarques

Les nœuds de document suivants ne sont pas comparés pour le moment :

* [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag)
* Article3

Les documents ne doivent pas avoir de révisions avant la comparaison.

### Exemples

Montre comment comparer des documents.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// La comparaison de documents avec des révisions lèvera une exception.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Après la comparaison, le document d'origine recevra une nouvelle révision
// pour chaque élément différent dans le document édité.
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// L'acceptation de ces révisions transformera le document d'origine en document modifié.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Voir également

* class [Document](../../document)
* espace de noms [Aspose.Words](../../document)
* Assemblée [Aspose.Words](../../../)

---

## Compare(Document, string, DateTime, CompareOptions) {#compare_1}

Compare ce document avec un autre document produisant des modifications sous la forme d'un certain nombre de révisions d'édition et de mise en forme[`Revision`](../../revision) . Permet de spécifier les options de comparaison à l'aide[`CompareOptions`](../../../aspose.words.comparing/compareoptions) .

```csharp
public void Compare(Document document, string author, DateTime dateTime, CompareOptions options)
```

### Exemples

Montre comment filtrer des types spécifiques d'éléments de document lors d'une comparaison.

```csharp
// Crée le document d'origine et le remplit avec différents types d'éléments.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Texte de paragraphe référencé avec une note de fin :
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// Table:
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

// Crée un clone de notre document et effectue une modification rapide sur chacun des éléments du document cloné.
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
// Un objet CompareOptions a une série de drapeaux qui peuvent supprimer les révisions
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

* class [CompareOptions](../../../aspose.words.comparing/compareoptions)
* class [Document](../../document)
* espace de noms [Aspose.Words](../../document)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
