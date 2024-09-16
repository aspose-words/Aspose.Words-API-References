---
title: DocumentBase.styles property
linktitle: styles property
articleTitle: styles property
second_title: Aspose.Words for Python
description: "DocumentBase.styles property. Returns a collection of styles defined in the document."
type: docs
weight: 90
url: /python-net/aspose.words/documentbase/styles/
---

## DocumentBase.styles property

Returns a collection of styles defined in the document.


```python
@property
def styles(self) -> aspose.words.StyleCollection:
    ...

```

### Remarks

For more information see the description of the [StyleCollection](../../stylecollection/) class.




### Examples

Shows how to create and use a paragraph style with list formatting.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Create a custom paragraph style.
style = doc.styles.add(aw.StyleType.PARAGRAPH, 'MyStyle1')
style.font.size = 24
style.font.name = 'Verdana'
style.paragraph_format.space_after = 12
# Create a list and make sure the paragraphs that use this style will use this list.
style.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
style.list_format.list_level_number = 0
# Apply the paragraph style to the document builder's current paragraph, and then add some text.
builder.paragraph_format.style = style
builder.writeln('Hello World: MyStyle1, bulleted list.')
# Change the document builder's style to one that has no list formatting and write another paragraph.
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.writeln('Hello World: Normal.')
builder.document.save(file_name=ARTIFACTS_DIR + 'Styles.ParagraphStyleBulletedList.docx')
```

Shows how to access a document's style collection.

```python
doc = aw.Document()
self.assertEqual(4, doc.styles.count)
# Enumerate and list all the styles that a document created using Aspose.Words contains by default.
for cur_style in doc.styles:
    print(f'Style name:\t"{cur_style.name}", of type "{cur_style.type}"')
    print(f'\tSubsequent style:\t{cur_style.next_paragraph_style_name}')
    print(f'\tIs heading:\t\t\t{cur_style.is_heading}')
    print(f'\tIs QuickStyle:\t\t{cur_style.is_quick_style}')
    self.assertEqual(doc, cur_style.document)
```

### See Also

* module [aspose.words](../../)
* class [DocumentBase](../)
* class [StyleCollection](../../stylecollection/)
* class [Style](../../style/)

