---
title: css_class_names_prefix property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies prefix which is added to all class names in style.css file"
type: docs
weight: 20
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/css_class_names_prefix/
---

## HtmlFixedSaveOptions.css_class_names_prefix property

Specifies prefix which is added to all class names in style.css file.
Default value is ``"aw"``.



### Examples

Shows how to place CSS into a separate file and add a prefix to all of its CSS class names.

```python
doc = aw.Document(MY_DIR + "Bookmarks.docx")

html_fixed_save_options = aw.saving.HtmlFixedSaveOptions()
html_fixed_save_options.css_class_names_prefix = "myprefix"
html_fixed_save_options.save_font_face_css_separately = True

doc.save(ARTIFACTS_DIR + "HtmlFixedSaveOptions.add_css_class_names_prefix.html", html_fixed_save_options)

with open(ARTIFACTS_DIR + "HtmlFixedSaveOptions.add_css_class_names_prefix.html", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

self.assertRegex(out_doc_contents,
    '<div class="myprefixdiv myprefixpage" style="width:595[.]3pt; height:841[.]9pt;">' +
    '<div class="myprefixdiv" style="left:85[.]05pt; top:36pt; clip:rect[(]0pt,510[.]25pt,74[.]95pt,-85.05pt[)];">' +
    '<span class="myprefixspan myprefixtext001" style="font-size:11pt; left:294[.]73pt; top:0[.]36pt; line-height:12[.]29pt;">')

with open(ARTIFACTS_DIR + "HtmlFixedSaveOptions.add_css_class_names_prefix/styles.css", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

self.assertRegex(out_doc_contents,
    ".myprefixdiv { position:absolute; } " +
    ".myprefixspan { position:absolute; white-space:pre; color:#000000; font-size:12pt; }")
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

