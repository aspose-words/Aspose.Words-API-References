---
title: TxtListIndentation.character property
linktitle: character property
articleTitle: character property
second_title: Aspose.Words for Python
description: "TxtListIndentation.character property. Gets or sets which character to use for indenting list levels"
type: docs
weight: 20
url: /sv/python-net/aspose.words.saving/txtlistindentation/character/
---

## TxtListIndentation.character property

Gets or sets which character to use for indenting list levels.
The default value is '\\0', that means there is no indentation.


```python
@property
def character(self) -> str:
    ...

@character.setter
def character(self, value: str):
    ...

```

### Examples

Shows how to configure list indenting when saving a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Skapa en lista med tre nivåer av indrag.
builder.list_format.apply_number_default()
builder.writeln('Item 1')
builder.list_format.list_indent()
builder.writeln('Item 2')
builder.list_format.list_indent()
builder.write('Item 3')
# Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur vi sparar dokumentet som klartext.
txt_save_options = aw.saving.TxtSaveOptions()
# Ställ in egenskapen "Character" för att tilldela ett tecken att använda
# för utfyllnad som simulerar listindrag i vanlig text.
txt_save_options.list_indentation.character = ' '
# Ställ in egenskapen "Count" för att ange antalet gånger
# för att placera utfyllnadstecknet för varje listindragnivå.
txt_save_options.list_indentation.count = 3
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.TxtListIndentation.txt', save_options=txt_save_options)
doc_text = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'TxtSaveOptions.TxtListIndentation.txt')
new_line = system_helper.environment.Environment.new_line()
self.assertEqual(f'1. Item 1{new_line}' + f'   a. Item 2{new_line}' + f'      i. Item 3{new_line}', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtListIndentation](../)

