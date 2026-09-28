---
title: Story.last_paragraph property
linktitle: last_paragraph property
articleTitle: last_paragraph property
second_title: Aspose.Words for Python
description: "Story.last_paragraph property. Gets the last paragraph in the story."
type: docs
weight: 20
url: /fr/python-net/aspose.words/story/last_paragraph/
---

## Story.last_paragraph property

Gets the last paragraph in the story.


```python
@property
def last_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# Le constructeur de document possède un curseur, qui agit comme la partie du document
# où le constructeur ajoute de nouveaux nœuds lorsque nous utilisons ses méthodes de construction de document.
# Ce curseur fonctionne de la même manière que le curseur clignotant de Microsoft Word,
# et il se retrouve toujours immédiatement après tout nœud que le constructeur vient d'insérer.
# Pour ajouter du contenu à une autre partie du document,
# nous pouvons déplacer le curseur vers un nœud différent avec la méthode "MoveTo".
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# Le curseur est maintenant devant le nœud vers lequel nous l'avons déplacé.
# Ajouter un deuxième segment l'insérera devant le premier segment.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# Déplacez le curseur à la fin du document pour continuer à ajouter du texte à la fin comme auparavant.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

