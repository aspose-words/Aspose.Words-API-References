---
title: HtmlSaveOptions.export_language_information property
linktitle: export_language_information property
articleTitle: export_language_information property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_language_information property. Specifies whether language information is exported to HTML, MHTML or EPUB"
type: docs
weight: 180
url: /python-net/aspose.words.saving/htmlsaveoptions/export_language_information/
---

## HtmlSaveOptions.export_language_information property

Specifies whether language information is exported to HTML, MHTML or EPUB.
Default is ``False``.



```python
@property
def export_language_information(self) -> bool:
    ...

@export_language_information.setter
def export_language_information(self, value: bool):
    ...

```

### Remarks

When this property is set to ``True`` Aspose.Words outputs **lang** HTML attribute on the document
elements that specify language. This can be needed to preserve language related semantics.




### Examples

Shows how to preserve language information when saving to .html.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Use the builder to write text while formatting it in different locales.
builder.font.locale_id = 1033  # en-US
builder.writeln('Hello world!')
builder.font.locale_id = 2057  # en-GB
builder.writeln('Hello again!')
builder.font.locale_id = 1049  # ru-RU
builder.write('Привет, мир!')
# When saving the document to HTML, we can pass a SaveOptions object
# to either preserve or discard each formatted text's locale.
# If we set the "export_language_information" flag to "True",
# the output HTML document will contain the locales in "lang" attributes of <span> tags.
# If we set the "export_language_information" flag to "False',
# the text in the output HTML document will not contain any locale information.
options = aw.saving.HtmlSaveOptions()
options.export_language_information = export_language_information
options.pretty_format = True
doc.save(ARTIFACTS_DIR + 'HtmlSaveOptions.export_language_information.html', options)
with open(ARTIFACTS_DIR + 'HtmlSaveOptions.export_language_information.html', 'rt', encoding='utf-8') as file:
    out_doc_contents = file.read()
if export_language_information:
    self.assertIn('<span>Hello world!</span>', out_doc_contents)
    self.assertIn('<span lang="en-GB">Hello again!</span>', out_doc_contents)
    self.assertIn('<span lang="ru-RU">Привет, мир!</span>', out_doc_contents)
else:
    self.assertIn('<span>Hello world!</span>', out_doc_contents)
    self.assertIn('<span>Hello again!</span>', out_doc_contents)
    self.assertIn('<span>Привет, мир!</span>', out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

