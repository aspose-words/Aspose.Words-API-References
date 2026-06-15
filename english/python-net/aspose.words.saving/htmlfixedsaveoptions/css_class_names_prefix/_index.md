---
title: HtmlFixedSaveOptions.css_class_names_prefix property
linktitle: css_class_names_prefix property
articleTitle: css_class_names_prefix property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.css_class_names_prefix property. Specifies prefix which is added to all class names in style.css file"
type: docs
weight: 20
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/css_class_names_prefix/
---

## HtmlFixedSaveOptions.css_class_names_prefix property

Specifies prefix which is added to all class names in style.css file.
Default value is ``"aw"``.



```python
@property
def css_class_names_prefix(self) -> str:
    ...

@css_class_names_prefix.setter
def css_class_names_prefix(self, value: str):
    ...

```

### Examples

Shows how to place CSS into a separate file and add a prefix to all of its CSS class names.

```python
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
import aspose.words as aw
import system_helper
import re
from unittest import TestCase
Assert = TestCase()
doc = aw.Document(MY_DIR + 'Bookmarks.docx')
html_fixed_save_options = aw.saving.HtmlFixedSaveOptions()
html_fixed_save_options.css_class_names_prefix = 'myprefix'
html_fixed_save_options.save_font_face_css_separately = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlFixedSaveOptions.AddCssClassNamesPrefix.html', save_options=html_fixed_save_options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.AddCssClassNamesPrefix.html')
Assert.assertTrue(re.search('<div class="myprefixdiv myprefixpage" style="width:595[.]3pt; height:841[.]9pt;">' + '<div class="myprefixdiv" style="left:85[.]05pt; top:36pt; clip:rect[(]0pt,510[.]25pt,74[.]95pt,-85.05pt[)];">' + '<span class="myprefixspan myprefixtext001" style="font-size:11pt; left:294[.]73pt; top:0[.]36pt; line-height:12[.]29pt;">', out_doc_contents) is not None)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css')
Assert.assertTrue(re.search('\\.myprefixdiv \\{ position:absolute; \\} ' + '\\.myprefixspan \\{ position:absolute; white-space:pre; color:#000000; font-size:12pt; \\}', out_doc_contents) is not None)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

