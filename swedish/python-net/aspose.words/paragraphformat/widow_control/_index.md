---
title: ParagraphFormat.widow_control property
linktitle: widow_control property
articleTitle: widow_control property
second_title: Aspose.Words for Python
description: "ParagraphFormat.widow_control property. True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph."
type: docs
weight: 410
url: /sv/python-net/aspose.words/paragraphformat/widow_control/
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
# När vi skriver text som inte får plats på en sida kan en rad rinna över till nästa sida.
# Den enda raden som hamnar på nästa sida kallas en "Orphan",
# och föregående rad där orphanen bröts av kallas en "Widow".
# Vi kan åtgärda orphans och widows genom att omarrangera text via teckenstorlek, avstånd eller sidmarginaler.
# Om vi vill bevara dokumentets dimensioner kan vi sätta denna flagga till "true"
# för att flytta widows till samma sida som deras respektive orphans.
# Att lämna denna flagga som "false" kommer att lämna widow/orphan-par i texten.
# Varje stycke har denna inställning tillgänglig i Microsoft Word via Start -> Stycke -> Styckeinställningar
# (knapp i nedre högra hörnet av fliken "Paragraph") -> "Widow/Orphan control".
builder.paragraph_format.widow_control = widow_control
# Infoga text som skapar en orphan och en widow.
builder.font.size = 68
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.WidowControl.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

