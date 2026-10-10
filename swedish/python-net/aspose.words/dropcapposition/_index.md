---
title: DropCapPosition enumeration
linktitle: DropCapPosition enumeration
articleTitle: DropCapPosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.DropCapPosition enumeration. Specifies the position for a drop cap text."
type: docs
weight: 350
url: /sv/python-net/aspose.words/dropcapposition/
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
# Infoga ett stycke med en stor bokstav som texten i det andra och tredje stycket börjar med.
builder.font.size = 54
builder.writeln('L')
builder.font.size = 18
builder.writeln('orem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ')
builder.writeln('Ut enim ad minim veniam, quis nostrud exercitation ' + 'ullamco laboris nisi ut aliquip ex ea commodo consequat.')
# För närvarande kommer det andra och tredje stycket att visas under det första.
# Vi kan konvertera det första stycket till en drop cap för de andra styckena via dess "ParagraphFormat"-objekt.
# Ställ in egenskapen "DropCapPosition" till "DropCapPosition.Margin" för att placera drop cap
# utanför den vänstra sidmarginalen om vår text är vänster-till-höger.
# Ställ in egenskapen "DropCapPosition" till "DropCapPosition.Normal" för att placera drop cap inom sidmarginalerna
# och för att låta resten av texten flöda runt den.
# "DropCapPosition.None" är standardläget för alla stycken.
format = doc.first_section.body.first_paragraph.paragraph_format
format.drop_cap_position = drop_cap_position
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.DropCap.docx')
```

### See Also

* module [aspose.words](../)

