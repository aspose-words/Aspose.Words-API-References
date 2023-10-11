---
title: InlineStory.EnsureMinimum
second_title: Référence de l'API Aspose.Words pour .NET
description: InlineStory méthode. Si le dernier enfant nest pas un paragraphe crée et ajoute un paragraphe vide.
type: docs
weight: 120
url: /fr/net/aspose.words/inlinestory/ensureminimum/
---
## InlineStory.EnsureMinimum method

Si le dernier enfant n'est pas un paragraphe, crée et ajoute un paragraphe vide.

```csharp
public void EnsureMinimum()
```

### Exemples

Montre comment insérer des nœuds InlineStory.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// Les nœuds de table ont une méthode "EnsureMinimum()" qui garantit que la table contient au moins une cellule.
Table table = new Table(doc);
table.EnsureMinimum();

// On peut placer un tableau à l'intérieur d'une note de bas de page, ce qui le fera apparaître en pied de page de référence.
Assert.That(footnote.Tables, Is.Empty);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// Un InlineStory possède également une méthode "EnsureMinimum()", mais dans ce cas,
// il s'assure que le dernier enfant du nœud est un paragraphe,
// pour que nous puissions cliquer et écrire du texte facilement dans Microsoft Word.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// Modifie l'apparence de l'ancre, qui est le petit numéro en exposant
// dans le texte principal qui pointe vers la note de bas de page.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// Tous les nœuds d'histoire en ligne ont leurs types d'histoire respectifs.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// Un commentaire est un autre type d'histoire en ligne.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// Le paragraphe parent d'un nœud d'histoire en ligne sera celui du corps principal du document.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// Cependant, le dernier paragraphe est celui du contenu du texte du commentaire,
// qui sera en dehors du corps principal du document dans une bulle.
// Un commentaire n'aura aucun nœud enfant par défaut,
// afin que nous puissions appliquer la méthode EnsureMinimum() pour placer un paragraphe ici également.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// Une fois que nous avons un paragraphe, nous pouvons déplacer le constructeur pour le faire et écrire notre commentaire.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### Voir également

* class [InlineStory](../)
* espace de noms [Aspose.Words](../../inlinestory/)
* Assemblée [Aspose.Words](../../../)


