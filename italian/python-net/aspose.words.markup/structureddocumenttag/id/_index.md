---
title: StructuredDocumentTag.id property
linktitle: id property
articleTitle: id property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.id property. Specifies a unique read-only persistent numerical Id for this SDT."
type: docs
weight: 140
url: /it/python-net/aspose.words.markup/structureddocumenttag/id/
---

## StructuredDocumentTag.id property

Specifies a unique read-only persistent numerical Id for this **SDT**.




```python
@property
def id(self) -> int:
    ...

```

### Remarks

Id attribute shall follow these rules:

* The document shall retain SDT ids only if the whole document is cloned [Document.clone()](../../../aspose.words/document/clone/#bool).
  
* During [DocumentBase.import_node()](../../../aspose.words/documentbase/import_node/#node_bool)
  Id shall be retained if import does not cause conflicts with other SDT Ids in
  the target document.
  
* If multiple SDT nodes specify the same decimal number value for the Id attribute,
  then the first SDT in the document shall maintain this original Id,
  and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
  
* During standalone SDT Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener) operation new unique ID will be generated for the cloned SDT node.
  
* If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned
  to it when the document is loaded.
  





### Examples

Shows how to create a structured document tag in a plain text box and modify its appearance.

```python
doc = aw.Document()
# Crea un tag di documento strutturato che conterrà testo semplice.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Imposta il titolo e il colore del riquadro che appare quando si passa il mouse sul tag di documento strutturato in Microsoft Word.
tag.title = 'My plain text'
tag.color = aspose.pydrawing.Color.magenta
# Imposta un tag per questo tag di documento strutturato, che è ottenibile
# come elemento XML denominato "tag", con la stringa sottostante nel suo attributo "@val".
tag.tag = 'MyPlainTextSDT'
# Ogni tag di documento strutturato ha un ID unico casuale.
self.assertTrue(tag.id > 0)
# Imposta il carattere per il testo all'interno del tag di documento strutturato.
tag.contents_font.name = 'Arial'
# Imposta il carattere per il testo alla fine del tag di documento strutturato.
# Qualsiasi testo che digitiamo nel corpo del documento dopo aver uscito dal tag con i tasti freccia utilizzerà questo carattere.
tag.end_character_font.name = 'Arial Black'
# Per impostazione predefinita, è false e premere Invio mentre si è all'interno di un tag di documento strutturato non fa nulla.
# Quando impostato su true, il nostro tag di documento strutturato può avere più righe.
# Imposta la proprietà "Multiline" su "false" per consentire solo il contenuto
# di questo tag di documento strutturato di occupare una sola riga.
# Imposta la proprietà "Multiline" su "true" per consentire al tag di contenere più righe di contenuto.
tag.multiline = True
# Imposta la proprietà "Appearance" su "SdtAppearance.Tags" per mostrare i tag attorno al contenuto.
# Per impostazione predefinita il tag di documento strutturato viene mostrato come BoundingBox.
tag.appearance = aw.markup.SdtAppearance.TAGS
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
# Inserisci un clone del nostro tag di documento strutturato in un nuovo paragrafo.
tag_clone = tag.clone(True).as_structured_document_tag()
builder.insert_paragraph()
builder.insert_node(tag_clone)
# Usa il metodo "RemoveSelfOnly" per rimuovere un tag di documento strutturato, mantenendo i suoi contenuti nel documento.
tag_clone.remove_self_only()
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlainText.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

