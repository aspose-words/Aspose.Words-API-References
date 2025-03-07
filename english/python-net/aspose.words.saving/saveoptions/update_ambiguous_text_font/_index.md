---
title: SaveOptions.update_ambiguous_text_font property
linktitle: update_ambiguous_text_font property
articleTitle: update_ambiguous_text_font property
second_title: Aspose.Words for Python
description: "SaveOptions.update_ambiguous_text_font property. Determines whether the font attributes will be changed according to the character code being used."
type: docs
weight: 130
url: /python-net/aspose.words.saving/saveoptions/update_ambiguous_text_font/
---

## SaveOptions.update_ambiguous_text_font property

Determines whether the font attributes will be changed according to the character code being used.


```python
@property
def update_ambiguous_text_font(self) -> bool:
    ...

@update_ambiguous_text_font.setter
def update_ambiguous_text_font(self, value: bool):
    ...

```

### Examples

Shows how to update the font to match the character code being used.

```python
doc = aw.Document(file_name=MY_DIR + 'Special symbol.docx')
run = doc.first_section.body.first_paragraph.runs[0]
print(run.text)  # ฿
print(run.font.name)  # Arial
save_options = aw.saving.OoxmlSaveOptions()
save_options.update_ambiguous_text_font = True
doc.save(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.UpdateAmbiguousTextFont.docx', save_options=save_options)
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.UpdateAmbiguousTextFont.docx')
run = doc.first_section.body.first_paragraph.runs[0]
print(run.text)  # ฿
print(run.font.name)  # Angsana New
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

