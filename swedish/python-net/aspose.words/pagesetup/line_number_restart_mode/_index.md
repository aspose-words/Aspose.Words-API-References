---
title: PageSetup.line_number_restart_mode property
linktitle: line_number_restart_mode property
articleTitle: line_number_restart_mode property
second_title: Aspose.Words for Python
description: "PageSetup.line_number_restart_mode property. Gets or sets the way line numbering runs  that is, whether it starts over at the beginning of a new page or section or runs continuously."
type: docs
weight: 230
url: /sv/python-net/aspose.words/pagesetup/line_number_restart_mode/
---

## PageSetup.line_number_restart_mode property

Gets or sets the way line numbering runs  that is, whether it starts over at the beginning of a new
page or section or runs continuously.


```python
@property
def line_number_restart_mode(self) -> aspose.words.LineNumberRestartMode:
    ...

@line_number_restart_mode.setter
def line_number_restart_mode(self, value: aspose.words.LineNumberRestartMode):
    ...

```

### Examples

Shows how to enable line numbering for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Vi kan använda sektionens PageSetup-objekt för att visa siffror till vänster om sektionens textrader.
# Detta är samma beteende som ett List-objekt,
# men det täcker hela sektionen och ändrar inte texten på något sätt.
# Vår sektion kommer att återställa numreringen på varje ny sida från 1 och visa numret,
# om det är en multipel av 3, på 50pt till vänster om raden.
page_setup = builder.page_setup
page_setup.line_starting_number = 1
page_setup.line_number_count_by = 3
page_setup.line_number_restart_mode = aw.LineNumberRestartMode.RESTART_PAGE
page_setup.line_number_distance_from_text = 50
i = 1
while i <= 25:
    builder.writeln(f'Line {i}.')
    i += 1
# Radräknaren kommer att hoppa över alla stycken med flaggan "SuppressLineNumbers" satt till "true".
# Detta stycke är på den 15:e raden, vilket är en multipel av 3, och skulle därför normalt visa ett radnummer.
# Avsnittets radräknare kommer också att ignorera den här raden, behandla nästa rad som den 15:e,
# och fortsätt räkningen från den punkten och framåt.
doc.first_section.body.paragraphs[14].paragraph_format.suppress_line_numbers = True
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.LineNumbers.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

