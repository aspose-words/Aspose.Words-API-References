---
title: ParagraphFormat.widow_control property
linktitle: widow_control property
articleTitle: widow_control property
second_title: Aspose.Words for Python
description: "ParagraphFormat.widow_control property. True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph."
type: docs
weight: 410
url: /de/python-net/aspose.words/paragraphformat/widow_control/
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
# Wenn wir den Text schreiben, der nicht auf eine Seite passt, kann eine Zeile auf die nächste Seite überlaufen.
# Die einzelne Zeile, die auf der nächsten Seite endet, wird als "Orphan" bezeichnet,
# und die vorherige Zeile, an der das Orphan abbricht, wird als "Widow" bezeichnet.
# Wir können Orphans und Widows beheben, indem wir den Text durch Schriftgröße, Abstand oder Seitenränder neu anordnen.
# Wenn wir die Abmessungen unseres Dokuments beibehalten möchten, können wir dieses Flag auf "true" setzen
# um Widows auf dieselbe Seite wie ihre jeweiligen Orphans zu verschieben.
# Wenn dieses Flag auf "false" bleibt, bleiben Widow/Orphan-Paare im Text erhalten.
# Jeder Absatz hat diese Einstellung, die in Microsoft Word über Start -> Absatz -> Absatzeinstellungen zugänglich ist
# (Schaltfläche in der unteren rechten Ecke des "Paragraph"-Tabs) -> "Widow/Orphan control".
builder.paragraph_format.widow_control = widow_control
# Fügen Sie Text ein, der ein Orphan und eine Widow erzeugt.
builder.font.size = 68
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.WidowControl.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

