---
title: ParagraphFormat.widow_control property
linktitle: widow_control property
articleTitle: widow_control property
second_title: Aspose.Words for Python
description: "ParagraphFormat.widow_control property. True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph."
type: docs
weight: 410
url: /it/python-net/aspose.words/paragraphformat/widow_control/
---

## ParagraphFormat.widow_control property

True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.


```python
@property
def widow_control(self) -> bool:
    ...

@widow_control.setter
def widow_control(self, value: bool):
    ...

```

### Examples

Shows how to enable widow/orphan control for a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Quando scriviamo il testo che non entra in una pagina, una riga può traboccare nella pagina successiva.
# La singola riga che finisce nella pagina successiva è chiamata "Orphan",
# e la riga precedente dove l'Orphan si è interrotta è chiamata "Widow".
# Possiamo correggere orfani e vedove riorganizzando il testo tramite dimensione del carattere, spaziatura o margini di pagina.
# Se desideriamo preservare le dimensioni del nostro documento, possiamo impostare questo flag su "true"
# per spostare le vedove sulla stessa pagina dei rispettivi orfani.
# Lasciare questo flag su "false" manterrà le coppie vedova/orfano nel testo.
# Ogni paragrafo ha questa impostazione accessibile in Microsoft Word tramite Home -> Paragraph -> Paragraph Settings
# (pulsante nell'angolo in basso a destra della scheda "Paragraph") -> "Widow/Orphan control".
builder.paragraph_format.widow_control = widow_control
# Inserisci del testo che genera un orfano e una vedova.
builder.font.size = 68
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.WidowControl.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

