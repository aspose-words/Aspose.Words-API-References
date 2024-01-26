---
title: Document.copy_styles_from_template method
linktitle: copy_styles_from_template method
articleTitle: copy_styles_from_template method
second_title: Aspose.Words for Python
description: "aspose.words.Document.copy_styles_from_template method"
type: docs
weight: 600
url: /python-net/aspose.words/document/copy_styles_from_template/
---

## copy_styles_from_template(template) {#str}

Copies styles from the specified template to a document.


```python
def copy_styles_from_template(self, template: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| template | str |  |

### Remarks

When styles are copied from a template to a document,
like-named styles in the document are redefined to match the style descriptions in the template.
Unique styles from the template are copied to the document. Unique styles in the document remain intact.


## copy_styles_from_template(template) {#document}

Copies styles from the specified template to a document.


```python
def copy_styles_from_template(self, template: aspose.words.Document):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| template | [Document](../) |  |

### Remarks

When styles are copied from a template to a document,
like-named styles in the document are redefined to match the style descriptions in the template.
Unique styles from the template are copied to the document. Unique styles in the document remain intact.


## Examples

Shows how to copy styles from one document to another.

```python
# Create a document, and then add styles that we will copy to another document.
template = aw.Document()

style = template.styles.add(aw.StyleType.PARAGRAPH, "TemplateStyle1")
style.font.name = "Times New Roman"
style.font.color = drawing.Color.navy

style = template.styles.add(aw.StyleType.PARAGRAPH, "TemplateStyle2")
style.font.name = "Arial"
style.font.color = drawing.Color.deep_sky_blue

style = template.styles.add(aw.StyleType.PARAGRAPH, "TemplateStyle3")
style.font.name = "Courier New"
style.font.color = drawing.Color.royal_blue

self.assertEqual(7, template.styles.count)

# Create a document which we will copy the styles to.
target = aw.Document()

# Create a style with the same name as a style from the template document and add it to the target document.
style = target.styles.add(aw.StyleType.PARAGRAPH, "TemplateStyle3")
style.font.name = "Calibri"
style.font.color = drawing.Color.orange

self.assertEqual(5, target.styles.count)

# There are two ways of calling the method to copy all the styles from one document to another.
# 1 -  Passing the template document object:
target.copy_styles_from_template(template)

# Copying styles adds all styles from the template document to the target
# and overwrites existing styles with the same name.
self.assertEqual(7, target.styles.count)

self.assertEqual("Courier New", target.styles.get_by_name("TemplateStyle3").font.name)
self.assertEqual(drawing.Color.royal_blue.to_argb(), target.styles.get_by_name("TemplateStyle3").font.color.to_argb())

# 2 -  Passing the local system filename of a template document:
target.copy_styles_from_template(MY_DIR + "Rendering.docx")

self.assertEqual(21, target.styles.count)
```

Shows how to copies styles from the template to a document via Document.

```python
template = aw.Document(MY_DIR + "Rendering.docx")
target = aw.Document(MY_DIR + "Document.docx")


target.copy_styles_from_template(template)
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

