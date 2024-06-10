---
title: DocumentBase.page_color property
linktitle: page_color property
articleTitle: page_color property
second_title: Aspose.Words for Python
description: "DocumentBase.page_color property. Gets or sets the page color of the document"
type: docs
weight: 50
url: /python-net/aspose.words/documentbase/page_color/
---

## DocumentBase.page_color property

Gets or sets the page color of the document. This property is a simpler version of [DocumentBase.background_shape](../background_shape/).



```python
@property
def page_color(self) -> aspose.pydrawing.Color:
    ...

@page_color.setter
def page_color(self, value: aspose.pydrawing.Color):
    ...

```

### Remarks

This property provides a simple way to specify a solid page color for the document.
Setting this property creates and sets an appropriate [DocumentBase.background_shape](../background_shape/).

If the page color is not set (e.g. there is no background shape in the document) returns
aspose.pydrawing.Color.empty.




### Examples

Shows how to set the background color for all pages of a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Hello world!')
doc.page_color = aspose.pydrawing.Color.light_gray
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBase.SetPageColor.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBase](../)
* property [DocumentBase.background_shape](../background_shape/)

