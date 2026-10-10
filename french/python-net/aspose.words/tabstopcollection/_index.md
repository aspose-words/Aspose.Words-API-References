---
title: TabStopCollection class
linktitle: TabStopCollection class
articleTitle: TabStopCollection class
second_title: Aspose.Words for Python
description: "aspose.words.TabStopCollection class. A collection of [TabStop](../tabstop/) objects that represent custom tabs for a paragraph or a style"
type: docs
weight: 1310
url: /fr/python-net/aspose.words/tabstopcollection/
---

## TabStopCollection class

A collection of [TabStop](../tabstop/) objects that represent custom tabs for a paragraph or a style.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/python-net/aspose-words-document-object-model/) documentation article.




### Remarks

In Microsoft Word documents, a tab stop can be defined in the properties of a paragraph
style or directly in the properties of a paragraph. A style can be based on another style.
Therefore, the complete set of tab stops for a given object is a combination of tab stops
defined directly on this object and tab stops inherited from the parent styles.

In Aspose.Words, when you obtain a [TabStopCollection](./) for a paragraph or a style,
it contains only the custom tab stops defined directly for this paragraph or style.
The collection does not include tab stops defined in the parent styles or default tab stops.




**Inheritance:** [TabStopCollection](./) → [InternableComplexAttr](../internablecomplexattr/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets a tab stop at the given index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of tab stops in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(tab_stop)](./add/#tabstop) | Adds or replaces a tab stop in the collection. |
|[ add(position, alignment, leader)](./add/#float_tabalignment_tableader) | Adds or replaces a tab stop in the collection. |
|[ after(position)](./after/#float) | Gets a first tab stop to the right of the specified position. |
|[ before(position)](./before/#float) | Gets a first tab stop to the left of the specified position. |
|[ clear()](./clear/#default) | Deletes all tab stop positions. |
|[ equals(rhs)](./equals/#tabstopcollection) | Determines whether the specified [TabStopCollection](./) is equal in value to the current [TabStopCollection](./). |
|[ get_index_by_position(position)](./get_index_by_position/#float) | Gets the index of a tab stop with the specified position in points. |
|[ get_position_by_index(index)](./get_position_by_index/#int) | Gets the position (in points) of the tab stop at the specified index. |
|[ remove_by_index(index)](./remove_by_index/#int) | Removes a tab stop at the specified index from the collection. |
|[ remove_by_position(position)](./remove_by_position/#float) | Removes a tab stop at the specified position from the collection. |

### Examples

Shows how to work with a document's collection of tab stops.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
tab_stops = builder.paragraph_format.tab_stops
# 72 points correspondent à un \"pouce\" sur la règle de tabulation de Microsoft Word.
tab_stops.add(tab_stop=aw.TabStop(position=72))
tab_stops.add(tab_stop=aw.TabStop(position=432, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.DASHES))
self.assertEqual(2, tab_stops.count)
self.assertFalse(tab_stops[0].is_clear)
self.assertFalse(tab_stops[0].equals(tab_stops[1]))
# Chaque caractère \"tab\" déplace le curseur du constructeur vers l'emplacement de l'arrêt de tabulation suivant.
builder.writeln('Start\tTab 1\tTab 2')
paragraphs = doc.first_section.body.paragraphs
self.assertEqual(2, paragraphs.count)
# Chaque paragraphe obtient sa collection d'arrêts de tabulation, qui clone ses valeurs à partir de la collection d'arrêts de tabulation du constructeur de document.
self.assertEqual(paragraphs[0].paragraph_format.tab_stops, paragraphs[1].paragraph_format.tab_stops)
# Une collection d'arrêts de tabulation peut nous indiquer les TabStops avant et après certaines positions.
self.assertEqual(72, tab_stops.before(100).position)
self.assertEqual(432, tab_stops.after(100).position)
# Nous pouvons effacer la collection d'arrêts de tabulation d'un paragraphe pour revenir au comportement de tabulation par défaut.
paragraphs[1].paragraph_format.tab_stops.clear()
self.assertEqual(0, paragraphs[1].paragraph_format.tab_stops.count)
doc.save(file_name=ARTIFACTS_DIR + 'TabStopCollection.TabStopCollection.docx')
```

### See Also

* module [aspose.words](../)
* class [InternableComplexAttr](../internablecomplexattr/)
* class [ParagraphFormat](../paragraphformat/)
* class [TabStop](../tabstop/)
* property [Document.default_tab_stop](../document/default_tab_stop/)

