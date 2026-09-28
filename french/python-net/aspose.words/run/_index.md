---
title: Run class
linktitle: Run class
articleTitle: Run class
second_title: Aspose.Words for Python
description: "aspose.words.Run class. Represents a run of characters with the same font formatting"
type: docs
weight: 1110
url: /fr/python-net/aspose.words/run/
---

## Run class

Represents a run of characters with the same font formatting.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




### Remarks

All text of the document is stored in runs of text.

[Run](./) can only be a child of [Paragraph](../paragraph/) or inline [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).




**Inheritance:** [Run](./) → [Inline](../inline/) → [Node](../node/)

### Constructors
| Name | Description |
| --- | --- |
| [Run(doc)](./__init__/#documentbase) | Initializes a new instance of the [Run](./) class. |
| [Run(doc, text)](./__init__/#documentbase_str) | Initializes a new instance of the **Run** class. |

### Properties

| Name | Description |
| --- | --- |
| [custom_node_id](../node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [font](../inline/font/) | Provides access to the font formatting of this object.<br>(Inherited from [Inline](../inline/)) |
| [is_composite](../node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [is_delete_revision](../inline/is_delete_revision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [is_format_revision](../inline/is_format_revision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [is_insert_revision](../inline/is_insert_revision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [is_move_from_revision](../inline/is_move_from_revision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [is_move_to_revision](../inline/is_move_to_revision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [is_phonetic_guide](./is_phonetic_guide/) | Gets a boolean value indicating either the run is a phonetic guide. |
| [next_sibling](../node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [node_type](./node_type/) | Returns [NodeType.RUN](../nodetype/#RUN). |
| [parent_node](../node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [parent_paragraph](../inline/parent_paragraph/) | Retrieves the parent [Paragraph](../paragraph/) of this node.<br>(Inherited from [Inline](../inline/)) |
| [phonetic_guide](./phonetic_guide/) | Gets a [Run.phonetic_guide](./phonetic_guide/) object. |
| [previous_sibling](../node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |
| [text](./text/) | Gets or sets the text of the run. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ clone(is_clone_children)](../node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#object) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ get_text()](./get_text/#default) | Gets the text of the run. |
|[ next_pre_order(root_node)](../node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ node_type_to_string(node_type)](../node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ previous_pre_order(root_node)](../node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_format)](../node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_options)](../node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### Examples

Shows how to format a run of text using its font property.

```python
doc = aw.Document()
run = aw.Run(doc=doc, text='Hello world!')
font = run.font
font.name = 'Courier New'
font.size = 36
font.highlight_color = aspose.pydrawing.Color.yellow
doc.first_section.body.first_paragraph.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.CreateFormattedRun.docx')
```

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```python
doc = aw.Document()
# Un document vide, par défaut, contient un paragraphe.
self.assertEqual(1, doc.first_section.body.paragraphs.count)
# Les nœuds composites tels que notre paragraphe peuvent contenir d'autres nœuds composites et en ligne comme enfants.
paragraph = doc.first_section.body.first_paragraph
paragraph_text = aw.Run(doc=doc, text='Initial text. ')
paragraph.append_child(paragraph_text)
# Créez trois nœuds d'exécution supplémentaires.
run1 = aw.Run(doc=doc, text='Run 1. ')
run2 = aw.Run(doc=doc, text='Run 2. ')
run3 = aw.Run(doc=doc, text='Run 3. ')
# Le corps du document n'affichera pas ces exécutions tant que nous ne les insérerons pas dans un nœud composite
# qui lui-même fait partie de l'arborescence des nœuds du document, comme nous l'avons fait avec la première exécution.
# Nous pouvons déterminer où le contenu texte des nœuds que nous insérons
# apparaît dans le document en spécifiant un emplacement d'insertion relatif à un autre nœud du paragraphe.
self.assertEqual('Initial text.', paragraph.get_text().strip())
# Insérez la deuxième exécution dans le paragraphe devant l'exécution initiale.
paragraph.insert_before(run2, paragraph_text)
self.assertEqual('Run 2. Initial text.', paragraph.get_text().strip())
# Insérez la troisième exécution après l'exécution initiale.
paragraph.insert_after(run3, paragraph_text)
self.assertEqual('Run 2. Initial text. Run 3.', paragraph.get_text().strip())
# Insérez la première exécution au début de la collection des nœuds enfants du paragraphe.
paragraph.prepend_child(run1)
self.assertEqual('Run 1. Run 2. Initial text. Run 3.', paragraph.get_text().strip())
self.assertEqual(4, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
# Nous pouvons modifier le contenu de l'exécution en modifiant et en supprimant les nœuds enfants existants.
paragraph.get_child_nodes(aw.NodeType.RUN, True)[1].as_run().text = 'Updated run 2. '
paragraph.get_child_nodes(aw.NodeType.RUN, True).remove(paragraph_text)
self.assertEqual('Run 1. Updated run 2. Run 3.', paragraph.get_text().strip())
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
```

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()
# Un document vierge contient une section, un corps et un paragraphe.
# Appelez la méthode "RemoveAllChildren" pour supprimer tous ces nœuds,
# et vous vous retrouvez avec un nœud de document sans enfants.
doc.remove_all_children()
# Ce document n'a maintenant aucun nœud enfant composite auquel nous pouvons ajouter du contenu.
# Si nous souhaitons le modifier, nous devrons reconstituer sa collection de nœuds.
# Tout d'abord, créez une nouvelle section, puis ajoutez‑la en tant qu'enfant au nœud racine du document.
section = aw.Section(doc)
doc.append_child(section)
# Définissez quelques propriétés de mise en page pour la section.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# Une section nécessite un corps, qui contiendra et affichera tout son contenu
# sur la page entre l'en‑tête et le pied‑de‑page de la section.
body = aw.Body(doc)
section.append_child(body)
# Créez un paragraphe, définissez quelques propriétés de formatage, puis ajoutez‑le en tant qu'enfant au corps.
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# Enfin, ajoutez du contenu au document. Créez un run,
# définissez son apparence et son contenu, puis ajoutez‑le en tant qu'enfant au paragraphe.
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../)
* class [Inline](../inline/)

