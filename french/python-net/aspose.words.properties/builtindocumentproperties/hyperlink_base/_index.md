---
title: BuiltInDocumentProperties.hyperlink_base property
linktitle: hyperlink_base property
articleTitle: hyperlink_base property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.hyperlink_base property. Specifies the base string used for evaluating relative hyperlinks in this document."
type: docs
weight: 130
url: /fr/python-net/aspose.words.properties/builtindocumentproperties/hyperlink_base/
---

## BuiltInDocumentProperties.hyperlink_base property

Specifies the base string used for evaluating relative hyperlinks in this document.


```python
@property
def hyperlink_base(self) -> str:
    ...

@hyperlink_base.setter
def hyperlink_base(self, value: str):
    ...

```

### Remarks

Aspose.Words does not use this property.




### Examples

Shows how to store the base part of a hyperlink in the document's properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insérez un hyperlien relatif vers un document du système de fichiers local nommé "Document.docx".
# Cliquer sur le lien dans Microsoft Word ouvrira le document désigné, s'il est disponible.
builder.insert_hyperlink('Relative hyperlink', 'Document.docx', False)
# Ce lien est relatif. S'il n'y a pas de "Document.docx" dans le même dossier
# comme le document qui contient ce lien, le lien sera rompu.
self.assertFalse(system_helper.io.File.exist(ARTIFACTS_DIR + 'Document.docx'))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.BrokenLink.docx')
# Le document que nous essayons de lier se trouve dans un répertoire différent de celui où nous prévoyons d'enregistrer le document.
# Nous pourrions corriger les liens de cette façon en mettant un nom de fichier absolu dans chacun d'eux.
# Alternativement, nous pourrions fournir un lien de base que chaque hyperlien avec un nom de fichier relatif
# préfixera à son lien lorsque nous cliquerons dessus.
properties = doc.built_in_document_properties
properties.hyperlink_base = MY_DIR
self.assertTrue(system_helper.io.File.exist(properties.hyperlink_base + doc.range.fields[0].as_field_hyperlink().address))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.WorkingLink.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

