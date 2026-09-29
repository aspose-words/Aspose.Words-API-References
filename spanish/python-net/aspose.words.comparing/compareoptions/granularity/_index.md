---
title: CompareOptions.granularity property
linktitle: granularity property
articleTitle: granularity property
second_title: Aspose.Words for Python
description: "CompareOptions.granularity property. Specifies whether changes are tracked by character or by word."
type: docs
weight: 40
url: /es/python-net/aspose.words.comparing/compareoptions/granularity/
---

## CompareOptions.granularity property

Specifies whether changes are tracked by character or by word.


```python
@property
def granularity(self) -> aspose.words.comparing.Granularity:
    ...

@granularity.setter
def granularity(self, value: aspose.words.comparing.Granularity):
    ...

```

### Remarks

Default value is [Granularity.WORD_LEVEL](../../granularity/#WORD_LEVEL).



### Examples

Shows to specify a granularity while comparing documents.

```python
doc_a = aw.Document()
builder_a = aw.DocumentBuilder(doc=doc_a)
builder_a.writeln('Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit')
doc_b = aw.Document()
builder_b = aw.DocumentBuilder(doc=doc_b)
builder_b.writeln('Lorems ipsum dolor sit amet consectetur - "adipiscing" elit')
# Especificar si los cambios se están rastreando
# por carácter ('Granularity.CharLevel'), o por palabra ('Granularity.WordLevel').
compare_options = aw.comparing.CompareOptions()
compare_options.granularity = granularity
doc_a.compare(document=doc_b, author='author', date_time=datetime.datetime.now(), options=compare_options)
# La colección de grupos de revisión del primer documento contiene todas las diferencias entre los documentos.
groups = doc_a.revisions.groups
self.assertEqual(5, groups.count)
```

### See Also

* module [aspose.words.comparing](../../)
* class [CompareOptions](../)

