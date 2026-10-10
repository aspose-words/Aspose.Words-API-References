---
title: FieldBarcode.is_bookmark property
linktitle: is_bookmark property
articleTitle: is_bookmark property
second_title: Aspose.Words for Python
description: "FieldBarcode.is_bookmark property. Gets or sets whether [FieldBarcode.postal_address](../postal_address/) is the name of a bookmark."
type: docs
weight: 30
url: /fr/python-net/aspose.words.fields/fieldbarcode/is_bookmark/
---

## FieldBarcode.is_bookmark property

Gets or sets whether [FieldBarcode.postal_address](../postal_address/) is the name of a bookmark.



```python
@property
def is_bookmark(self) -> bool:
    ...

@is_bookmark.setter
def is_bookmark(self, value: bool):
    ...

```

### Examples

Shows how to use the BARCODE field to display U.S. ZIP codes in the form of a barcode.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln()
# Voici deux façons d'utiliser les champs BARCODE pour afficher des valeurs personnalisées sous forme de codes-barres.
# 1 -  Stockez la valeur que le code-barres affichera dans la propriété PostalAddress :
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BARCODE, update_field=True).as_field_barcode()
# Cette valeur doit être un code postal valide.
field.postal_address = '96801'
field.is_us_postal_address = True
field.facing_identification_mark = 'C'
self.assertEqual(' BARCODE  96801 \\u \\f C', field.get_field_code())
builder.insert_break(aw.BreakType.LINE_BREAK)
# 2 -  Référencez un signet qui stocke la valeur que ce code-barres affichera :
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BARCODE, update_field=True).as_field_barcode()
field.postal_address = 'BarcodeBookmark'
field.is_bookmark = True
self.assertEqual(' BARCODE  BarcodeBookmark \\b', field.get_field_code())
# Le signet que le champ BARCODE référence dans sa propriété PostalAddress
# doit contenir uniquement le code postal valide.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('BarcodeBookmark')
builder.writeln('968877')
builder.end_bookmark('BarcodeBookmark')
doc.save(file_name=ARTIFACTS_DIR + 'Field.BARCODE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldBarcode](../)

