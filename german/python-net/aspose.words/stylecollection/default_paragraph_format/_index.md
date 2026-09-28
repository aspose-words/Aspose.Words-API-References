---
title: StyleCollection.default_paragraph_format property
linktitle: default_paragraph_format property
articleTitle: default_paragraph_format property
second_title: Aspose.Words for Python
description: "StyleCollection.default_paragraph_format property. Gets document default paragraph formatting."
type: docs
weight: 40
url: /de/python-net/aspose.words/stylecollection/default_paragraph_format/
---

## StyleCollection.default_paragraph_format property

Gets document default paragraph formatting.


```python
@property
def default_paragraph_format(self) -> aspose.words.ParagraphFormat:
    ...

```

### Remarks

Note that document-wide defaults were introduced in Microsoft Word 2007 and are fully supported in OOXML formats ([LoadFormat.DOCX](../../loadformat/#DOCX)) only.
Earlier document formats have no support for document default paragraph formatting.




### Examples

Shows how to add a Style to a document's styles collection.

```python
doc = aw.Document()
styles = doc.styles
# Legen Sie Standardparameter für neue Stile fest, die wir später zu dieser Sammlung hinzufügen können.
styles.default_font.name = 'Courier New'
# Wenn wir einen Stil vom Typ \"StyleType.Paragraph\" hinzufügen, wendet die Sammlung die Werte von
# seiner \"DefaultParagraphFormat\"-Eigenschaft auf die \"ParagraphFormat\"-Eigenschaft des Stils an.
styles.default_paragraph_format.first_line_indent = 15
# Fügen Sie einen Stil hinzu und prüfen Sie anschließend, dass er die Standardeinstellungen hat.
styles.add(aw.StyleType.PARAGRAPH, 'MyStyle')
self.assertEqual('Courier New', styles[4].font.name)
self.assertEqual(15, styles.get_by_name('MyStyle').paragraph_format.first_line_indent)
```

### See Also

* module [aspose.words](../../)
* class [StyleCollection](../)

