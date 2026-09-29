---
title: DropCapPosition enumeration
linktitle: DropCapPosition enumeration
articleTitle: DropCapPosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.DropCapPosition enumeration. Specifies the position for a drop cap text."
type: docs
weight: 350
url: /it/python-net/aspose.words/dropcapposition/
---

## DropCapPosition enumeration

Specifies the position for a drop cap text.


### Members

| Name | Description |
| --- | --- |
| NONE | The paragraph does not have a drop cap. |
| NORMAL | The drop cap is positioned inside the text margin on the anchor paragraph. |
| MARGIN | The drop cap is positioned outside the text margin on the anchor paragraph. |

### Examples

Shows how to create a drop cap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci un paragrafo con una lettera grande con cui inizia il testo nei secondi e terzi paragrafi.
builder.font.size = 54
builder.writeln('L')
builder.font.size = 18
builder.writeln('orem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ')
builder.writeln('Ut enim ad minim veniam, quis nostrud exercitation ' + 'ullamco laboris nisi ut aliquip ex ea commodo consequat.')
# Attualmente, il secondo e il terzo paragrafo appariranno sotto il primo.
# Possiamo convertire il primo paragrafo in una capoverso iniziale per gli altri paragrafi tramite il suo oggetto "ParagraphFormat".
# Imposta la proprietà "DropCapPosition" su "DropCapPosition.Margin" per posizionare il drop cap
# al di fuori del margine sinistro della pagina se il nostro testo è da sinistra a destra.
# Imposta la proprietà "DropCapPosition" su "DropCapPosition.Normal" per posizionare il drop cap all'interno dei margini della pagina
# e per avvolgere il resto del testo attorno ad esso.
# "DropCapPosition.None" è lo stato predefinito per tutti i paragrafi.
format = doc.first_section.body.first_paragraph.paragraph_format
format.drop_cap_position = drop_cap_position
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.DropCap.docx')
```

### See Also

* module [aspose.words](../)

