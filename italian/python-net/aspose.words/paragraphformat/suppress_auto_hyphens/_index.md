---
title: ParagraphFormat.suppress_auto_hyphens property
linktitle: suppress_auto_hyphens property
articleTitle: suppress_auto_hyphens property
second_title: Aspose.Words for Python
description: "ParagraphFormat.suppress_auto_hyphens property. Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings."
type: docs
weight: 380
url: /it/python-net/aspose.words/paragraphformat/suppress_auto_hyphens/
---

## ParagraphFormat.suppress_auto_hyphens property

Specifies whether the current paragraph should be exempted from any hyphenation which
is applied in the document settings.


```python
@property
def suppress_auto_hyphens(self) -> bool:
    ...

@suppress_auto_hyphens.setter
def suppress_auto_hyphens(self, value: bool):
    ...

```

### Examples

Shows how to suppress hyphenation for a paragraph.

```python
aw.Hyphenation.register_dictionary(language='de-CH', file_name=MY_DIR + 'hyph_de_CH.dic')
self.assertTrue(aw.Hyphenation.is_dictionary_registered('de-CH'))
# Apri un documento contenente testo con una localizzazione corrispondente a quella del nostro dizionario.
# Quando salviamo questo documento in un formato di salvataggio a pagina fissa, il suo testo avrà la sillabazione.
doc = aw.Document(file_name=MY_DIR + 'German text.docx')
# Possiamo impostare la proprietà "SuppressAutoHyphens" su "true" per disabilitare la sillabazione
# per un paragrafo specifico mantenendola abilitata per il resto del documento.
# Il valore predefinito per questa proprietà è "false",
# il che significa che, per impostazione predefinita, ogni paragrafo utilizza la sillabazione se disponibile.
doc.first_section.body.first_paragraph.paragraph_format.suppress_auto_hyphens = suppress_auto_hyphens
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.SuppressHyphens.pdf')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

