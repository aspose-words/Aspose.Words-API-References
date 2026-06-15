---
title: BuiltInDocumentProperties.template property
linktitle: template property
articleTitle: template property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.template property. Gets or sets the informational name of the document template."
type: docs
weight: 300
url: /python-net/aspose.words.properties/builtindocumentproperties/template/
---

## BuiltInDocumentProperties.template property

Gets or sets the informational name of the document template.


```python
@property
def template(self) -> str:
    ...

@template.setter
def template(self, value: str):
    ...

```

### Remarks

In Microsoft Word, this property is for informational purposes only and
usually contains only the file name of the template without the path.

Empty string means the document is attached to the Normal template.

To get or set the actual name of the attached template, use the
[Document.attached_template](../../../aspose.words/document/attached_template/) property.




### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)
* property [Document.attached_template](../../../aspose.words/document/attached_template/)

