---
title: StructuredDocumentTag.remove_self_only method
linktitle: remove_self_only method
articleTitle: remove_self_only method
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.remove_self_only method. Removes just this SDT node itself, but keeps the content of it inside the document tree."
type: docs
weight: 370
url: /it/python-net/aspose.words.markup/structureddocumenttag/remove_self_only/
---

## remove_self_only() {#default}

Removes just this SDT node itself, but keeps the content of it inside the document tree.


```python
def remove_self_only(self):
    ...
```

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

