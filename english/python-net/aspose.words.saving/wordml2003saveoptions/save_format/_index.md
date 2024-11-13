---
title: WordML2003SaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "WordML2003SaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 20
url: /python-net/aspose.words.saving/wordml2003saveoptions/save_format/
---

## WordML2003SaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.WORD_ML](../../../aspose.words/saveformat/#WORD_ML).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to manage output document's raw content.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Create a "WordML2003SaveOptions" object to pass to the document's "Save" method
# to modify how we save the document to the WordML save format.
options = aw.saving.WordML2003SaveOptions()
self.assertEqual(aw.SaveFormat.WORD_ML, options.save_format)
# Set the "PrettyFormat" property to "true" to apply tab character indentation and
# newlines to make the output document's raw content easier to read.
# Set the "PrettyFormat" property to "false" to save the document's raw content in one continuous body of the text.
options.pretty_format = pretty_format
doc.save(file_name=ARTIFACTS_DIR + 'WordML2003SaveOptions.PrettyFormat.xml', save_options=options)
file_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'WordML2003SaveOptions.PrettyFormat.xml')
if pretty_format:
    self.assertTrue('<o:DocumentProperties>\r\n\t\t' + '<o:Revision>1</o:Revision>\r\n\t\t' + '<o:TotalTime>0</o:TotalTime>\r\n\t\t' + '<o:Pages>1</o:Pages>\r\n\t\t' + '<o:Words>0</o:Words>\r\n\t\t' + '<o:Characters>0</o:Characters>\r\n\t\t' + '<o:Lines>1</o:Lines>\r\n\t\t' + '<o:Paragraphs>1</o:Paragraphs>\r\n\t\t' + '<o:CharactersWithSpaces>0</o:CharactersWithSpaces>\r\n\t\t' + '<o:Version>11.5606</o:Version>\r\n\t' + '</o:DocumentProperties>' in file_contents)
else:
    self.assertTrue('<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>' + '<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>' + '<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>' in file_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [WordML2003SaveOptions](../)

