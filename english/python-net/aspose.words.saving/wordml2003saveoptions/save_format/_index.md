---
title: save_format property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 20
url: /python-net/aspose.words.saving/wordml2003saveoptions/save_format/
---

## WordML2003SaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.WORD_ML](../../../aspose.words/saveformat/#WORD_ML).



### Examples

Shows how to manage output document's raw content.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world!")

# Create a "WordML2003SaveOptions" object to pass to the document's "save" method
# to modify how we save the document to the WordML save format.
options = aw.saving.WordML2003SaveOptions()

self.assertEqual(aw.SaveFormat.WORD_ML, options.save_format)

# Set the "pretty_format" property to "True" to apply tab character indentation and
# newlines to make the output document's raw content easier to read.
# Set the "pretty_format" property to "False" to save the document's raw content in one continuous body of the text.
options.pretty_format = pretty_format

doc.save(ARTIFACTS_DIR + "WordML2003SaveOptions.pretty_format.xml", options)

with open(ARTIFACTS_DIR + "WordML2003SaveOptions.pretty_format.xml", "rb") as file:
    file_contents = file.read().decode('utf-8')

if pretty_format:
    expected = (
        "<o:DocumentProperties>\r\n\t\t" +
            "<o:Revision>1</o:Revision>\r\n\t\t" +
            "<o:TotalTime>0</o:TotalTime>\r\n\t\t" +
            "<o:Pages>1</o:Pages>\r\n\t\t" +
            "<o:Words>0</o:Words>\r\n\t\t" +
            "<o:Characters>0</o:Characters>\r\n\t\t" +
            "<o:Lines>1</o:Lines>\r\n\t\t" +
            "<o:Paragraphs>1</o:Paragraphs>\r\n\t\t" +
            "<o:CharactersWithSpaces>0</o:CharactersWithSpaces>\r\n\t\t" +
            "<o:Version>11.5606</o:Version>\r\n\t" +
        "</o:DocumentProperties>")
    self.assertTrue(expected in file_contents)
else:
    expected = (
        "<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>" +
        "<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" +
        "<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>")
    self.assertTrue(expected in file_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [WordML2003SaveOptions](../)

