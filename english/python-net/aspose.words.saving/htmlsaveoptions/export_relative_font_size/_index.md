---
title: HtmlSaveOptions.export_relative_font_size property
linktitle: export_relative_font_size property
articleTitle: export_relative_font_size property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_relative_font_size property. Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB"
type: docs
weight: 230
url: /python-net/aspose.words.saving/htmlsaveoptions/export_relative_font_size/
---

## HtmlSaveOptions.export_relative_font_size property

Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB.
Default is ``False``.



```python
@property
def export_relative_font_size(self) -> bool:
    ...

@export_relative_font_size.setter
def export_relative_font_size(self, value: bool):
    ...

```

### Remarks

In many existing documents (HTML, IDPF EPUB) font sizes are specified in relative units. This allows
applications to adjust text size when viewing/processing documents. For instance, Microsoft Internet Explorer
has "View-\>Text Size" submenu, Adobe Digital Editions has two buttons: Increase/Decrease Text Size.
If you expect this functionality to work then set [HtmlSaveOptions.export_relative_font_size](./) property to ``True``.


Aspose Words document model contains and operates only with absolute font size units. Relative units need 
additional logic to be recalculated from some initial (standard) size. Font size of **Normal** document style 
is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output 
as **1.5em.** to the HTML.

When this option is enabled, document elements other than text will still have absolute sizes. Also some 
text-related attributes might be expressed absolutely. In particular, line spacing specified with "exactly" rule 
might produce unwanted results when scaling text. So the source documents should be properly designed and tested 
when exporting with [HtmlSaveOptions.export_relative_font_size](./) set to ``True``.




### Examples

Shows how to use relative font sizes when saving to .html.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Default font size, ')
builder.font.size = 24
builder.writeln('2x default font size,')
builder.font.size = 96
builder.write('8x default font size')
# When we save the document to HTML, we can pass a SaveOptions object
# to determine whether to use relative or absolute font sizes.
# Set the "ExportRelativeFontSize" flag to "true" to declare font sizes
# using the "em" measurement unit, which is a factor that multiplies the current font size.
# Set the "ExportRelativeFontSize" flag to "false" to declare font sizes
# using the "pt" measurement unit, which is the font's absolute size in points.
options = aw.saving.HtmlSaveOptions()
options.export_relative_font_size = export_relative_font_size
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.RelativeFontSize.html', save_options=options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.RelativeFontSize.html')
if export_relative_font_size:
    self.assertTrue('<body style="font-family:\'Times New Roman\'">' + '<div>' + '<p style="margin-top:0pt; margin-bottom:0pt">' + '<span>Default font size, </span>' + '</p>' + '<p style="margin-top:0pt; margin-bottom:0pt; font-size:2em">' + '<span>2x default font size,</span>' + '</p>' + '<p style="margin-top:0pt; margin-bottom:0pt; font-size:8em">' + '<span>8x default font size</span>' + '</p>' + '</div>' + '</body>' in out_doc_contents)
else:
    self.assertTrue('<body style="font-family:\'Times New Roman\'; font-size:12pt">' + '<div>' + '<p style="margin-top:0pt; margin-bottom:0pt">' + '<span>Default font size, </span>' + '</p>' + '<p style="margin-top:0pt; margin-bottom:0pt; font-size:24pt">' + '<span>2x default font size,</span>' + '</p>' + '<p style="margin-top:0pt; margin-bottom:0pt; font-size:96pt">' + '<span>8x default font size</span>' + '</p>' + '</div>' + '</body>' in out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

