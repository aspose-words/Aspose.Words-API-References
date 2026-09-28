---
title: Field.display_result property
linktitle: display_result property
articleTitle: display_result property
second_title: Aspose.Words for Python
description: "Field.display_result property. Gets the text that represents the displayed field result."
type: docs
weight: 10
url: /de/python-net/aspose.words.fields/field/display_result/
---

## Field.display_result property

Gets the text that represents the displayed field result.


```python
@property
def display_result(self) -> str:
    ...

```

### Remarks

The [Document.update_list_labels()](../../../aspose.words/document/update_list_labels/#default) method must be called to obtain correct value for the
[FieldListNum](../../fieldlistnum/), [FieldAutoNum](../../fieldautonum/), [FieldAutoNumOut](../../fieldautonumout/) and [FieldAutoNumLgl](../../fieldautonumlgl/) fields.



### Examples

Shows how to get the real text that a field displays in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('This document was written by ')
field_author = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
field_author.author_name = 'John Doe'
# Wir können die DisplayResult-Eigenschaft verwenden, um den genauen Text zu überprüfen
# den ein Feld an seiner Stelle im Dokument anzeigen würde.
self.assertEqual('', field_author.display_result)
# Felder behalten keine genauen Ergebniswerte in Echtzeit bei.
# Um sicherzustellen, dass unsere Felder zu jedem Zeitpunkt genaue Ergebnisse anzeigen,
# zum Beispiel unmittelbar vor einem Speichervorgang, müssen wir sie manuell aktualisieren.
field_author.update()
self.assertEqual('John Doe', field_author.display_result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.DisplayResult.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [Field](../)

