---
title: SaveOptions.default_template property
linktitle: default_template property
articleTitle: default_template property
second_title: Aspose.Words for Python
description: "SaveOptions.default_template property. Gets or sets path to default template (including filename)"
type: docs
weight: 20
url: /de/python-net/aspose.words.saving/saveoptions/default_template/
---

## SaveOptions.default_template property

Gets or sets path to default template (including filename).
Default value for this property is **empty string** ().



```python
@property
def default_template(self) -> str:
    ...

@default_template.setter
def default_template(self, value: str):
    ...

```

### Remarks

If specified, this path is used to load template when [Document.automatically_update_styles](../../../aspose.words/document/automatically_update_styles/) is ``True``,
but [Document.attached_template](../../../aspose.words/document/attached_template/) is empty.


### Examples

Shows how to set a default template for documents that do not have attached templates.

```python
doc = aw.Document()
# Automatisches Aktualisieren von Stilen aktivieren, aber kein Vorlagendokument anhängen.
doc.automatically_update_styles = True
self.assertEqual('', doc.attached_template)
# Da es kein Vorlagendokument gibt, hatte das Dokument keinen Ort, um Stiländerungen zu verfolgen.
# Verwenden Sie ein SaveOptions‑Objekt, um automatisch eine Vorlage festzulegen
# falls ein Dokument, das wir speichern, keine hat.
options = aw.saving.SaveOptions.create_save_options(file_name='Document.DefaultTemplate.docx')
options.default_template = MY_DIR + 'Business brochure.dotx'
doc.save(file_name=ARTIFACTS_DIR + 'Document.DefaultTemplate.docx', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

