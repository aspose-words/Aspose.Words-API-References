---
title: FindReplaceOptions.ignore_fields property
linktitle: ignore_fields property
articleTitle: ignore_fields property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.ignore_fields property. Gets or sets a boolean value indicating either to ignore text inside fields"
type: docs
weight: 80
url: /fr/python-net/aspose.words.replacing/findreplaceoptions/ignore_fields/
---

## FindReplaceOptions.ignore_fields property

Gets or sets a boolean value indicating either to ignore text inside fields.
The default value is ``False``.



```python
@property
def ignore_fields(self) -> bool:
    ...

@ignore_fields.setter
def ignore_fields(self, value: bool):
    ...

```

### Remarks

This option affects whole field (all nodes between
[NodeType.FIELD_START](../../../aspose.words/nodetype/#FIELD_START) and [NodeType.FIELD_END](../../../aspose.words/nodetype/#FIELD_END)).

To ignore only field codes, please use corresponding option [FindReplaceOptions.ignore_field_codes](../ignore_field_codes/).




### Examples

Shows how to ignore text inside fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
builder.insert_field(field_code='QUOTE', field_value='Hello again!')
# Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et de remplacement.
options = aw.replacing.FindReplaceOptions()
# Définissez le drapeau "IgnoreFields" sur "true" pour obtenir l'opération de recherche-remplacement
# qui ignore le texte à l'intérieur des champs.
# Définissez le drapeau "IgnoreFields" sur "false" pour obtenir l'opération de recherche-remplacement
# qui recherche également le texte à l'intérieur des champs.
options.ignore_fields = ignore_text_inside_fields
doc.range.replace(pattern='Hello', replacement='Greetings', options=options)
self.assertEqual('Greetings world!\r\x13QUOTE\x14Hello again!\x15' if ignore_text_inside_fields else 'Greetings world!\r\x13QUOTE\x14Greetings again!\x15', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

