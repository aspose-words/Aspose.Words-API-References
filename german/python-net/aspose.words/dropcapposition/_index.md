---
title: DropCapPosition enumeration
linktitle: DropCapPosition enumeration
articleTitle: DropCapPosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.DropCapPosition enumeration. Specifies the position for a drop cap text."
type: docs
weight: 350
url: /de/python-net/aspose.words/dropcapposition/
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
# Füge einen Absatz mit einem großen Buchstaben ein, mit dem der Text im zweiten und dritten Absatz beginnt.
builder.font.size = 54
builder.writeln('L')
builder.font.size = 18
builder.writeln('orem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ')
builder.writeln('Ut enim ad minim veniam, quis nostrud exercitation ' + 'ullamco laboris nisi ut aliquip ex ea commodo consequat.')
# Derzeit erscheinen der zweite und dritte Absatz unter dem ersten.
# Wir können den ersten Absatz über sein "ParagraphFormat"-Objekt in einen Initialbuchstaben für die anderen Absätze umwandeln.
# Setze die Eigenschaft "DropCapPosition" auf "DropCapPosition.Margin", um den Initialbuchstaben zu platzieren
# außerhalb des linken Seitenrands, wenn unser Text von links nach rechts verläuft.
# Setze die Eigenschaft "DropCapPosition" auf "DropCapPosition.Normal", um den Initialbuchstaben innerhalb der Seitenränder zu platzieren
# und den restlichen Text darum fließen zu lassen.
# "DropCapPosition.None" ist der Standardzustand für alle Absätze.
format = doc.first_section.body.first_paragraph.paragraph_format
format.drop_cap_position = drop_cap_position
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.DropCap.docx')
```

### See Also

* module [aspose.words](../)

